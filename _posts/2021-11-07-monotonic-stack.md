---
layout: post
title: Monotonic Stack 101
excerpt: "What is a monotonic stack?"
modified: 2021-11-07
comments: true
---
Another post, another coding challenge.

The problem is simple:

> Given an array of integers, return an array such that `solution[i]` is the number of positions until a position `j` where `values[j] > values[i]`. 
If there is no `j` such that `values[j] > values[i]`, then `solution[i] == 0`.

What!? It's much simpler than that. This is known as the [daily temperatures](https://leetcode.com/problems/daily-temperatures/) problem in LeetCode.

![Temperatures](/images/monotonic-stack/temperatures.png)


Let's start with a naive solution and see later how can we do better!

## Naive solution

The simplest (and most inefficient in this case) thing that we can do, is to just check for every single element `i` in the given array,
 if there is an element with index `j` such that `j > i` and `values[j] > values[i]`. If we found such element, then the solution for `i`
 is the distance between `j` and `i` which is `j - i`.

 If we cannot find such element, then we don't need to do anything as `int[]` in Java are intialized with a 0 in each position.

{% highlight java %}
public int[] dailyTemperatures(int[] values) {
    int[] solution = new int[values.length];
    
    for (int i = 0; i < values.length ; i++) {
        for (int j = i + 1; j < values.length; j++) {
            if (values[j] > values[i]) {
                solution[i] = j - i;
                break;
            }
        }
    }
    
    return solution;
}
{% endhighlight %}

As you might imagine, the time complexity of this solution is O(n^2). This is because for each element, we need to potentially inspect all elements
ahead. So for `i = 0` we inspect `n` elements. For `i = 1` we inspect `n - 1`.

The recurrence relation for this process is: 

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">
  <mi>T</mi>
  <mo stretchy="false">(</mo>
  <mi>n</mi>
  <mo stretchy="false">)</mo>
  <mo>=</mo>
  <mrow>
    <mo>{</mo>
    <mtable columnalign="left left" rowspacing=".2em" columnspacing="1em" displaystyle="false">
      <mtr>
        <mtd>
          <mi mathvariant="normal">&#x0398;<!-- Θ --></mi>
             <mo stretchy="false">(</mo>
          <mn>1</mn>
          <mo stretchy="false">)</mo>
        </mtd>
        <mtd>
          <mrow class="MJX-TeXAtom-ORD">
            <mtext>if&#xA0;</mtext>
          </mrow>
          <mi>n</mi>
          <mo>=</mo>
          <mn>1</mn>
          <mo>,</mo>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mi>T</mi>
          <mo stretchy="false">(</mo>
          <mi>n</mi>
          <mo>&#x2212;<!-- − --></mo>
          <mn>1</mn>
          <mo stretchy="false">)</mo>
          <mo>+</mo>
          <mi mathvariant="normal">&#x0398;<!-- Θ --></mi>
          <mo stretchy="false">(</mo>
          <mi>n</mi>
          <mo stretchy="false">)</mo>
        </mtd>
        <mtd>
          <mrow class="MJX-TeXAtom-ORD">
            <mtext>if&#xA0;</mtext>
          </mrow>
          <mi>n</mi>
          <mo>&gt;</mo>
          <mn>1.</mn>
        </mtd>
      </mtr>
    </mtable>
    <mo fence="true" stretchy="true" symmetric="true"></mo>
  </mrow>
</math>

Because solving the problem `T(N)` involves a linear scan and then solving the same problem for one less element.


## Using a monotonic stack

Now we get into the juicy part. Can we do better than that? Yes we can but it's not going to be that simple.

We would like to solve this problem in the fastest way we can, which would be linear time as we need to provide an answer for every single element of the input, an array of size `N`.

Every time we process an element, the answer to the question "How far away is the next element greater than this one?" cannot be solved _yet_, as we haven't processed
those elements that lie ahead in the array. So what we are going to do is to store those elements in a stack so they can be processed later on.

The algorithm has 2 parts:
- Add current element to a stack so we can process it later.
- Check if the current element can be used to solve some of the previous unsolved items.

If at the top of the stack there is an element smaller than the current element, then
the distance between the top of the stack and the current element is the answer. Now that we know the answer, we can
remove that element from our "pending to be processed" stack.

Let's go through an example before jumping into the code:

- Our input array is `[4,3,1,6,5,7]`
- We construct a new array with the same size as the input to store our results `int[] result = new int[values.length];`.
- We declare a `new Stack<>()` that will help us processing the elements. 
- We process element index `0` and value `4`, and because the stack is empty we just put it in the stack to be processed later.
![Step 0](/images/monotonic-stack/0.png)

- We process element index `1` and value `3`. As `3` is smaller than the value referenced by the index at top of the stack `values[1] < values[0] == 3 < 4`,
then we don't do anything and just push index `1` onto the stack.

![Step 1](/images/monotonic-stack/1.png)

- Same as before for index `2`.

![Step 2](/images/monotonic-stack/2.png)


- Here things get interesting. Current index is `3` and the value is larger than the one referenced by the top of the stack `values[3] > values[2] == 6 > 1`.
- So we pop index `2` from the stack, and `result[2] = 3 - 2`.
- In code this would be `result[topOfStack] = current - topOfStack` where `topOfStack = 2` and `current  = 3`.

![Step 3](/images/monotonic-stack/3.png)

- Current index is still `3` but we haven't finished processing all the possible elements from the stack. 
- So we pop index `1` from the stack, and `result[1] = 3 - 1`.
- We do the same for index `0` and `result[0] = 3 - 0`.
- Finally we push index `3` as we cannot calculate `result[3]` yet.

![Step 5](/images/monotonic-stack/5.png)

- With the same logic as in the first steps, we push index `4` onto the stack.

![Step 6](/images/monotonic-stack/6.png)

- Current index is `5` and the value is larger than the one referenced by the top of the stack `values[5] > values[4]`.
- So we pop index `4` from the stack, and `result[4] = 5 - 4`.
- We finish processing the array and there is still an element in the Stack. Remember what I said about Java initialising
arrays with a `0` in every position? Due to that we don't need to do any processing for those elements that are still in the stack.

![Step 7](/images/monotonic-stack/7.png)


Let's see how that looks like in code:

{% highlight java %}
public int[] dailyTemperatures(int[] values) {
    Stack<Integer> stack = new Stack<>();
    int[] result = new int[values.length];
    
    for (int i = 0; i < values.length ; i++) {
        while (!stack.isEmpty() && values[stack.peek()] < values[i]) {
            int lastIndex = stack.pop();
            result[lastIndex] = i - lastIndex;
        }
        
        stack.push(i);
    }
    
    return result;
}
{% endhighlight %}

# The design flaw of Java Stack

In the previous code I used a Java `Stack` but the usage of this collection is disencouraged. Why? Java `Stack` inherits from `Vector`,
which is a clear violation of the [Liskov substition principle](https://en.wikipedia.org/wiki/Liskov_substitution_principle). This inheritance allows `Stack` users to use methods such as `stack.add(index, element)` which doesn't make sense for such data structure. 
An `Stack` should only allow users to push/pop elements to/from the top of the stack and that's it.


Both Stack and Vector were included with the first release of Java, so this flaw in the `Stack` design is something that has been carried
around for long time. The way `Java` fixed this flaw, is by introducing a proper `Deque<E>` interface in version 6.

`Stack` [documentation says](ttps://docs.oracle.com/javase/8/docs/api/java/util/Stack.html):

> A more complete and consistent set of LIFO stack operations is provided by the Deque interface and its implementations, which should be used in preference to this class. For example:

`Deque<Integer> stack = new ArrayDeque<Integer>();`


# Conclusion

A monotonic stack is a fancy name for a stack where we store values that are either monotonically increasing or decreasing 
(depending on our needs). The idea of remembering contiguous sequences so we can use them in the future when processing
other elements is both simple and powerful.

This solution runs in linear time `O(n)` as we only process each element once (think about how many items each element enters into the stack). 
Space complexity is also `O(n)` (don't even think about the result array), because in the worst case scenario our stack will be full with all 
the `N` elements to be processed. That would happen if the input array contains a monotonically decreasing sequence.

Still want more? Here you have a [list of coding challenges that can be solved by using a Monotonic Stack](https://leetcode.com/tag/monotonic-stack/).

Hope you liked the explanation!