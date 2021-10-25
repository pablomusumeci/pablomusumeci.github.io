---
layout: post
title: Count number of 1 bits on an Java int
excerpt: "Also known as calculating the hamming weight"
modified: 2021-10-25
comments: true
---

The problem is simple:

> Write a function that takes an unsigned integer and returns the number of '1' bits it has (also known as the Hamming weight).

What I really liked about this problem is that there are so many different ways to
get to the right answer. Usually this kind of coding chalenges depend on you knowning 
that _one trick_ that solves the question. So at the end it boils down to whether you
know the trick or not, which doesn't leave a lot of room for debating on alternative 
solutions.

In this post I'll walk through a variety of solutions while doing a brief analysis of each. Let's start!

## Integer.bitCount(n)

That's it. I think that if you are facing this problem during an interview, you can just mention this to your interviewer and that will show them 2 things:
- You know [Java APIs](https://docs.oracle.com/javase/7/docs/api/java/lang/Integer.html#bitCount(int). Always good to know the tools you have at your hand.
- Don't reinvent the wheel.

But probably this is not what your interviewer was looking for when they asked this question, so move on to some other solution as they probably will tell you:

> Cool... but lets imagine you cannot use this built-in method.

## Integer.toBinaryString(n)

If you are still afraid of bit manipulation (you shouldn't!), you can use this other [Integer API](https://docs.oracle.com/javase/7/docs/api/java/lang/Integer.html#toBinaryString(int)) that returns a string representation of the integer argument as an unsigned integer in base 2.

{% highlight java %}
Integer.toBinaryString(2); // "10"
{% endhighlight %}

As you can see, the returned String has no left padding. Not a problem for this question but in case you are curious on how you can achieve that:

{% highlight java %}
String padded = String.format("%32s", Integer.toBinaryString(2)); // "                              10"
padded.replace(' ', '0'); // "00000000000000000000000000000010"
{% endhighlight %}

Let's define that as a helper function that we will later use on this post.
{% highlight java %}
String leftPadded(int n) {
    return String.format("%32s", Integer.toBinaryString(n)).replace(' ', '0');
}
{% endhighlight %}


Now we can just iterate the String and count the occurences of '1'. Let's use the sleak Stream API to achieve that.
Note that there is no way of going from a `char[]` to a Stream, so we use an IntStream instead and just go with the flow.

{% highlight java %}
Integer.toBinaryString(2).chars().filter( c -> c == '1').count()
{% endhighlight %}

## Bit masking

This is the way I would solve the problem in an interview as it's the least magical clean and concise solution in my opinion. 
Trying to use a mystical algorithm you don't quite know or remember during an interview can easily back-fire if you cannot explain
what you are doing or even worse, you might not even get to the answer because you don't remember the algorithm details.

As Richard Feynmann says:

> What I cannot create, I do not understand.

The key aspect of this solution is using a [bit mask](https://en.wikipedia.org/wiki/Mask_(computing)). In plain english,
just put 1's in the places you care about and ignore the rest.

We are going to use a bit mask containing only one 1, but we are going to move the position of the mask through 32 possible
places as our problem demands us to count the amount of 1's in a 32 bit `int`.

{% highlight java %}
public int hammingWeight(int n) {    
    int count = 0;
    int mask = 1;
    // Do 31 bit shifts, from 0...0001 to 1...0000
    for (int bit = 0; bit < 32; bit++) {
        if ((n & mask << bit) >= 1) {
            count++;    
        }
    }
    
    return count;
}
{% endhighlight %}

We use `<<` to move the mask to the right. But sadly this solution will not work exactly as we expect.

Using `<<` bit shift operator has a catch. Java has 2 different types of bit shifting operators

### Arithmethic bit shifting

In an arithmetic shift, the sign bit is **extended** to preserve the signedness of the number. This means that if there
was a 1 on the first position of the bit representation, that 1 will be extended while shifting bits.

{% highlight java %}
leftPadded(-102937123);      // "11111001110111010100110111011101"
leftPadded(-102937123 >> 1); // "11111100111011101010011011101110"
{% endhighlight %}

Pay attention to the start of the String and see how the 1 is extended.

**111110**01110111010100110111011101
**111111**00111011101010011011101110

### Logical bit shifting

Now let's compare it against using the logical bit shift operator `<<<`

{% highlight java %}
leftPadded(-102937123);       // "11111001110111010100110111011101"
leftPadded(-102937123 >>> 1); // "01111100111011101010011011101110"
{% endhighlight %}

`<<<` or `>>>` don't care that the value could possibly represent a signed number; it simply moves everything to the left/right and fills in from the left with 0s. 

**111110**01110111010100110111011101
**011111**00111011101010011011101110

Now that we know this, we can fix our previous solution:

{% highlight java %}
public int hammingWeight(int n) {    
    int count = 0;
    int mask = 1;
    // Do 31 logical bit shifts, from 0...0001 to 1...0000
    for (int bit = 0; bit < 32; bit++) {
        if ((n & mask <<< bit) >= 1) {
            count++;    
        }
    }
    
    return count;
}
{% endhighlight %}

Our solution runs in constant time as it executes a fixed number of operations (at most 31 but the number is not important as long as it does not depend on the size of the input).

## Brian Kernighan's Algorithm

### Observation

Kernighan realised that subtracting 1 from a number flips all the bits after the rightmost set bit (included). What!?

```
10 in binary is 1010
9  in binary is 1001
8  in binary is 1000
7  in binary is 0111
6  in binary is 0110
5  in binary is 0101
4  in binary is 0100
3  in binary is 0011
2  in binary is 0010
1  in binary is 0001
```

Let's examine 9 and 8 where the case is very easy to observe. The rightmost bit is the 1 at the end, so only that one is flipped. This means that if the number is odd,
then substracting one will just convert that last 1 into a 0. 1001 converts into 1000.

Let's do 9 and 8 now. 1000 converts into 0111, so all the bits are flipped starting (and including) the rightmost set bit.

### Algorithm

Now that we know this, let's try to count the number of 1's in number 10.

```
10     in binary is 1010
9      in binary is 1001
10 & 9 in binary is 1000
```

If we pay attention to the result of `10 & 9 = 1000` we see that the least significant bit of `1010` dissapeared.
So what Kernighan's Algorithm is all about is executing `number & (number - 1)` until all bits have dissapeared.

{% highlight java %}
public int hammingWeight(int n) {    
    int count = 0;
    while( n != 0) {
        n &= n - 1;
        count++;
    }
    
    return count;
}
{% endhighlight %}

Kernighan's solution runs in constant time (same as bit masking) but it does the minimum amount of work neccesary as it only counts
the 1s without any extra work. 


# Conclusions

I don't think anybody expects an interviewee to know about Kernighan's clever algorithm to count bits. Moreover,
I think knowing about bit masking can help you solving many other similar problems involving bit manipulations.
Being said that, I still think that Kernighan's algorithm is pretty neat and that's why I wanted to mention it.

Hope you learned something by reading this because I'm sure I did while solving this challenge and preparing this blog post.