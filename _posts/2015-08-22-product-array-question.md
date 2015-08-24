---
layout: post
title: Product array interview question 
excerpt: "Tricky array interview question"
modified: 2015-08-22
comments: true
---

The other day I came across this tricky question:

> Given an array of numbers, return an array in which each element is equal
> to the product of all the numbers in the original array except for the element in that position.
> The use of the division operator is forbidden.

Lets try to clarify this with an example:
{% highlight python %}
#Given numbers array
numbers = [4, 9, 7, 5]
# Result shall be
result = [9 * 7 * 5, 4 * 7 * 5, 4 * 9 * 5, 4 * 9 * 7]
{% endhighlight %}

There is a naive solution for this problem which involves a \\( O(n^{2}) \\) execution order. 
This solution consists in iterating the whole array for each element we want to process, 
multiplying the element only if its index is not same as the original element. 

The code is simpler than the explanation: 
{% highlight python %}
def array_multiplication(array):
    result = []
    for i in xrange(len(array)):
        result.append(1)
        for j in xrange(len(array)):
            if j != i:
                result[i] *= array[j]
    return result
{% endhighlight %}

But we can do it a lot better. If we pay attention, we can notice a pattern in the
result array.

{% highlight python %}
result = [() * (9 * 7 * 5), (4) * (7 * 5), (4 * 9) * (5), (4 * 9 * 7) * ()]
{% endhighlight %}

Imagine that multiplying by the empty parenthesis is the same as multiplying by 1.

When we are iterating the original array, we can split it into 2 halves. The numbers
which we have already processed and the ones we haven't. 

The left half (a.k.a. the already processed group) starts as a empty group and grows
with each element we process. Moreover, the right half has a similar but opposite
pattern. It starts as "all the elements except the first one" and drops one element per
iteration until it becomes an empty set.

The trick here is that we cannot drop a number from the group using the division operator,
so we need to build left and right at the same time while iterating the original array.

To sum up, we are going to build 2 arrays (left and right) which will lead us to a 
solution for each index *i* as: result[i] = left[i] * right[i]

In the previous example left and right would have been:

{% highlight python %}
result = [() * (9 * 7 * 5), (4) * (7 * 5), (4 * 9) * (5), (4 * 9 * 7) * ()]
left = [1, 4, 4 * 9, 4 * 9 * 7]
right = [1, 5, 5 * 7, 5 * 7 * 9] # Remember to reverse this array!
# If we do the product between left and right reversed one element at a time:
#result[0] = left[0] * right[0] # (1) * (5 * 7 * 9)
#result[1] = left[1] * right[1] # (4) * (5 * 7)
#result[2] = left[2] * right[2] # (4 * 9) * (5)
#result[1] = left[1] * right[1] # (4 * 9 * 7) * (1)
{% endhighlight %}

Here you have the algorithm:

{% highlight python %}
def array_multiplication(array):
    # empthy () is equal to 1
    left, right = [1], [1]
    for i in xrange(1, len(array)):
        left.append(array[i-1] * left[i-1])
        right.append(array[len(array) - i] * right[i-1])
    return [l * r for l, r in zip(left, right[::-1])] 
{% endhighlight %}

If you have never heard about zip, it's just something Python gives us
for iterating 2 collections at the same time.

With this algorithm we reach to a \\( O(n) \\) solution both in execution time and
in extra space consumption.
