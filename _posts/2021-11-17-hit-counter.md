---
layout: post
title: Design a hit counter
excerpt: "AKA design a rate limiter"
modified: 2021-11-07
comments: true
---

# Description

Today's coding challenge is about designing a rate limiter in Java. We will go over 3 different implementations while discussing all the
trade-offs for each solution, the time and space complexity and also a deep dive into the code.

> Talk is cheap. Show me the code.
>
> -- <cite>Linus Torvalds</cite>


This an exercise I like both as an interviewer and as an interviewee due to the interesting discussions that might arise from each
different implementation. There is no silver bullet, so regardless of which solution you choose to implement during an interview it's important
to know the shortcomings of it and how can it be improved.


You can find this problem named as [hit counter](https://leetcode.com/problems/design-hit-counter/) in LeetCode. This code would be the 
basis for designing a rate limiting algorithm. Imagine that each hit received is a request coming to a server, and what we actually need
 to do is accounting on the amount of requests in different time windows and based on that we can determine if a request should be
 dropped or not.


![Hit Counter](/images/hit-counter/leetcode-hit-counter.png)

Enough chatting, let's jump into the code!

## Using a Queue

## Code

{% highlight java %}
class HitCounter {
    Queue<Integer> queue = new LinkedList<>();

    public void hit(int timestamp) {
        queue.add(timestamp);
    }

    public int getHits(int timestamp) {
        while (!queue.isEmpty() && timestamp - queue.peek() + 1 > 300) {
            queue.poll();
        }
        return queue.size();
    }
}
{% endhighlight %}

## Analysis

The simplest but also least efficient solution. Every `add` operation adds a new timestamp to the queue, so it's constant time.

Heavy-lifting happens during `get` operations as there we need to remove from the queue the timestamps that are already expired (in the worst-case
scenario this means removing all the elements, so `O(n)` time complexity and also `O(n)` of space being held).

Another caveat of this approach is that timestamps are not _compressed_. We will have in the queue an entry per each timestamp even 
if they are repeated, this uses much more memory than just counting the amount of occurences.

Visualize the difference in memory consumption between a list like `[1, 1, 1, 1, 1, 1]` to `{ 1 = 6 }`. This idea takes us to our next approach!

# Using a TreeMap 

{% highlight java %}
class HitCounter {
    private TreeMap<Integer, Integer> tree = new TreeMap<>();
    
    public void hit(int timestamp) {
        tree.put(timestamp, tree.getOrDefault(timestamp, 0) + 1);
    }
    
    public int getHits(int timestamp) {
        // Evict old entries
        tree = new TreeMap<>(tree.subMap(timestamp - 300, false, timestamp, true));
        return tree.values().stream().mapToInt(Integer::intValue).sum();
    }
}
{% endhighlight %}

## Analysis

This solution uses a balanced tree (`TreeMap` is implementated as a [red-black tree](https://en.wikipedia.org/wiki/Red%E2%80%93black_tree)) where the keys represent the timestamp in which a hit was detected, and the value
counts the amount of times a hit was received at that exact same timestamp. Because the tree is balanced, any `hit` operation
takes `O(log(n))` time for updating the tree.

What about getting the hit count? Every time we want to get the amount of hits we first evict old entries that don't fit in our `300 seconds` window anymore by replacing the entire tree with just a portion of that only contains the entries that should still be counted.

For that sake we use [subMap]
](https://docs.oracle.com/javase/8/docs/api/java/util/TreeMap.html#subMap-K-boolean-K-boolean-):
> Returns a view of the portion of this map whose keys range from fromKey to toKey.

Note: While I was writing this post I got curious and digged a bit deeper into the API. Turns out that `subMap` is still backed by the original map,
so the entries are not being cleared from memory. But because we construct a new copy from that view, then the old map will be unused and then it can be garbage collected.

As an alternative, We can execute the following line:

{% highlight java %}
tree.headMap(timestamp - 300, true).clear();
{% endhighlight %}

This line gets the view of the tree that should be evicted (the opposite from the previous operation where we wanted to retain all the keys that should not be evicted)
and just call `.clear()` to empty that view of the map. By doing this we save the effort of creating unnecesary copies of the map.

### Extra note

In the previous code we decided to execute our maintenace task (cleaning up the evicted entries from the map) just before retrieving the `hits`. We could have
also done it after the insertion of a new value. What changes? Well, it's an expensive operation so here you need to discuss about which case should the 
data structure be optimised for. Do we want fast reads and slow writes, or the other way around? In the ideal scenario we want everything to be fast, but in this solution
we need to make a compromise. Let's check our third and final solution that solves this problem.

# Using a circular array

{% highlight java %}
public class HitCounter {
    private int[] timestamps;
    private int[] hits;
    
    public HitCounter() {
        timestamps = new int[300];
        hits = new int[300];
    }
    
    public void hit(int timestamp) {
        // Index in a circular array
        int index = timestamp % 300;

        // Overwrite evicted entry
        if (timestamps[index] != timestamp) {
            timestamps[index] = timestamp;
            hits[index] = 1;
        } else {
            // Update existing entry
            hits[index]++;
        }
    }
    
    public int getHits(int timestamp) {
        int total = 0;
        for (int i = 0; i < 300; i++) {
            // Count if inside the window
            // Skip evicted entries
            if (timestamp - timestamps[i] < 300) {
                total += hits[i];
            }
        }
        return total;
    }
}
{% endhighlight %}

## How does a circular array works?

A circular array is just an array, but the way we use it is what makes it circular. 

Pay close attention to this line:

{% highlight java %}
int index = timestamp % 300;
{% endhighlight %}

Each timestamp will be mapped to a cell in our `hits` array. In order not to mix old and new entries, we will
keep another array `timestamps` where we store the timestamp associated to each index.

This extra array `timestamps` is necessary because without it, it would be impossible to tell if `hits[5]`
is refering to timestamp of `5`, `305`, `605`, etc. The beauty of this, is that all each one of those timestamps
belong to a completely separate `300` seconds window, but they live inside the same array.

Still unclear? Let's check a toy example with a 10 seconds window:

![Example](/images/hit-counter/example.png)

## Analysis

The most complex (not really, just until you understand the secret behind it) and also the most performant solution. The amount
of space used is constant `O(1)`. You might say, "Hey, that's not constant, is an array of 300 positions!". Well, that's true,
but those 300 positions do not depend on the amount of hits we receive but only on the time window selected. Our algorithm
doesn't care if we process 5 or 5 million hits, the amount of space used will remain constant.

Same applies for the time complexity of calculating the amount of hits. We aways iterate over the entire array to answer the query.

# Conclusion

Are those the only solutions to this problem? Not at all, but those are the ones that highlight different trade-offs and strategies
for solving this problem.