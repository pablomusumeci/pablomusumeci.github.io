---
title: Acing the software engineering interview - Part II
excerpt: FAANGtastic interviewing
last_modified_at: 2021-12-27
categories:
  - Software interviews  
tags:
  - Interviewing
  - LeetCode
toc: true
toc_label: Acing the SWE interview - Part II
toc_icon: code
toc_sticky: true
---

This is the second in a [series of blog posts](https://pablomusumeci.github.io/categories/#software-interviews) 
where I describe my interviewing experience and thoughts in detail.

In this post I'm going to dissect what is in my opinion the best platform for preparing coding interviews:

{:refdef: style="text-align: center;"}
![Leetcode](/assets/images/acing-the-software-engineering-interview/Leetcode-logo.png)
{: refdef}

By far the single most valuable tool I used during the entire preparation process. It works great out-of-the-box but if you want to get
the best out of it you need to use it wisely. Optimizing your learning process is key for fast improvement. Learn how to learn.

But first, what makes LeetCode so great?

# As real as it gets

LeetCode provides a plain text environment with no autocompletion (only syntax highlighting).
I have to admit it, my first time using the platform I couldn't even write a simple for-loop in Java. 
Typing even the most simple syntax without autocompletion felt so unnatural.
It's what it is. No secrets here, you need to get used to it. This is how you are going to be evaluated 
so better to be comfortable in that same kind of environment.

Your brain is so used to using the IDE features that you don't even know you are using them until you don't have them anymore.
You have to learn the basics again. Using breakpoints? Forget about it, here we think hard and use strategic prints to understand what's going on.

{:refdef: style="text-align: center;"}
![Blind](/assets/images/acing-the-software-engineering-interview/Blind.jpeg)
{: refdef}


You will have to know the APIs available in your language of choice. I became genuinely comfortable using things I had never used
at my job like [Arrays.deepToString](https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html#deepToString(java.lang.Object[])) or doing bit-shifting operations. It was unnatural until it wasn't anymore.

⚠️ Your interviewer doesn't expect you to know absolutely everything by heart. Everybody allowed me to google something if needed.
Of course you should ask them first if it's acceptable to do so.
Knowing APIs by heart allows you to think so much faster as you don't need to 
worry about details such as how to print an `int[][]` or the syntax for defining a custom `Comparator`. 
You have larger problems to solve during the interview than fighting against the language you have chosen. 
Showing proficiency there definitely helps. Maybe it doesn't impress your interviewer that you know your language
inside out but it projects a poor image of yourself if you have to google the basics.

# Mock assessments

It's a premium feature but one that makes going premium definitely worth it. With this _interviewing mode_ you get
a configurable amount of random exercises to solve in a fixed amount of time. You also have the opportunity of 
choosing a particular company so problems are taken from that company's pool reported by other LeetCode users.

{:refdef: style="text-align: center;"}
![assesment](/assets/images/acing-the-software-engineering-interview/assesment.png)
{: refdef}


Once you click the start button, there is no coming back. No pause, no bathroom break, no choosing the category or difficulty of the problems. 
Exactly as real interview would be. You want to [expose yourself](https://pablomusumeci.github.io/acing-the-software-engineering-interview-part-iii/#exposure-therapy) to thinking under pressure as much as possible. 
You can be a genius who designs elegant solutions but if you can't do that in 30 minutes then you will most 
likely fail the interview.

Once you've finished, you will receive a report with an evaluation of your performance compared to other candidates.

{:refdef: style="text-align: center;"}
![report](/assets/images/acing-the-software-engineering-interview/LeetCode-report.png)
{: refdef}

It also shows you an overview of your performance accross different areas and a nudge about where you should be focusing on.

{:refdef: style="text-align: center;"}
![overview](/assets/images/acing-the-software-engineering-interview/LeetCode-overview.png)
{: refdef}

:warning: Don't be too distracted by those scores if you are using LeetCode (and most people are) as preparation for interviewing.
The score is derived from the time complexity and memory usage of your solution. However, it will never take readability into account. Sometimes
the most efficient solution is the hardest to read, understand, extend or debug. You are being judged on those topics as well
even if they are not mentioned in the report. That doesn't mean interviewers will be satisfied with a readable brute-force solution but you get the point.

# Think and only then act

Impulse control is everything. When you have been coding non-stop for 15 minutes and feel that you've finished your algorithm, the immediate
urge is to hit the **RUN** button and hope to see that magic text saying <span style="color:green">**SUCCESS**</span>. Don't.

Once you've finished your coding you need to review the changes. Then review them again.

If you click **RUN** and get a dissappointing <span style="color:red">**FAILURE**</span> result, 
you will feel the natural urge of immediately fixing the obvious (best case scenario) bug and submitting again as fast as possible. 
It's the way our brains are wired, the dopamine rush we get when we triump at any task.

I'm not a fortune-teller but I'm quite confident that regularly you will find that many other bugs were hidding in your code 
waiting for their chance to suckerpunch you.
When something fails, take your time to analyze the problem and understand what happened. Not only the line that failed but the entire code again. 
If you missed that one single tiny thing, how can you be sure that you haven't missed many others?

{:refdef: style="text-align: center;"}
![stop-think-act](/assets/images/acing-the-software-engineering-interview/stop-think-act.jpeg)
{: refdef}

Your interviewers are judging what kind of programmer you are:

- Are you someone who stops to calmly think if there is more than meets the eye? Someone that carefully checks the code 
to understand what went wrong.

- Are you a hack-and-slash programmer? Someone who tries to duck tape the error by adding yet another if statement, submitting without
thinking and praying that this time all the test cases are 💚.

This is also valuable advice for your career. Every time I have to send a pull-request, I look at the same piece of code 
three different times using three different diff tools. More often than I would like to admit, I end up finding something 
I've missed in the previous self-review round.

If you don't restrain that urge of clicking **SUBMIT** and calling it for the day then you are abusing your reviewer's time.
They will have to flag all the issues that you could have fixed on your own if you had been a little bit more careful with your work.

# Free vs Premium

I started with a free subscription and I think everybody should do the same. That is more than enough to
get you started. One can only take true advantage of the premium features once you've solved a large amount of the basic problems offered by the platform.
I'm sorry but money can't accelerate your learning at the beginning.

After one month of using it 2 hours a day Monday to Sunday I finally decided to **invest** 35 USD (~30 euros) to get the best out of my time. 
I reasoned the cost was 1 euro per day which is close to nothing as I only planned to use it until I landed the job of my dreams.

Hopefully, the search was not going to take me forever although I had no pressure to change jobs quickly. 
My focus was on finding the best opportunity for my career and to get that I had become a master of my craft. LeetCode free version had
demostrated to be a powerful ally on that journey. If Premium features improved my preparation even slightly then it was already a worthy investment.

Premium gives you access to features like (sorted by importance for me):
- Premium questions
- Select questions by company
- [Timed assesments](#timed-assesments)
- Sorting questions by frequency
- Autocompletion
- No waiting time between submissions
- Official solutions
- Explore cards

Is it necessary? I guess not. Does it help a lot? Hell yeah! Likely the investment with the highest return you are going to
make in your life. $35 might be neglegible or not depending on where you live. But if LeetCode Premium helps you landing a better offer 
that gets you some extra money then it will pay by itself very quickly.

# Discussion section is the true gold mine
After you are done with a problem, regardless of solving it through terrible brute force solution or not solving it at all, 
you **must** enter the discussion forum. Doing that is not optional because there is where the magic happens.

In the discussion forum you will find that there were at least three complete different ways of solving the problem.
Different solutions with different trade-offs in terms of time and space complexity.
Probably the most performant solution is an already existing algorithm or obscure technique that no one 
can realistically come up with it during an interview unless they've seen it beforehand.
That's fine as no-one expects you to come up with such during an interview anyway. 

Nonetheless, reading and thinking about those solutions will expand your horizon about how problems can be solved. 
Those ideas can be leveraged in other problems because at some point [all problems start to look similar to one you've previously solved](#leetcode-templates).

I contributed to the discussion section as much as I could. Replying to questions, upvoting the best solutions and even posting my own.
Sometimes the core logic of my code was the same as another solution but I considered posting like submitting a pull-request at work.

It helped me to double-check my work and add comments to the non-straightforward parts of the code. Also forced myself to write a brief explanation of 
how the algorithm works in plain English. I use the [Feynmann technique](https://fs.blog/feynman-technique/) for diving deep into
my understanding of the solution. Sometimes I feel that I finally understood something and still I felt incapable of explaining it clearly.
That's a reality check where I come clean with myself about how much of the topic do I actually comprehend.

> Now that you think you understand a topic reasonably well, explain it to a 12-year-old.
>
> -- <cite>The Feynman Technique.</cite>

# LeetCode templates
The more problems you face, the more you start observing the hidden patterns that connect all of them together. 
There are thousands of different problems but only a handful of patterns.

Sometimes the pattern is hidden and it's up to you to uncover it. What do I mean by _hidden_? 
The way a problem is presented can make more or less obvious how it should be modeled. 
If you think about cities being connected by routes then it's intuitive to think about a graph where cities are nodes
and routes are edges connecting nodes.

Other times the representation of the solution space is not that obvious. In a finite state machine a given state is as a node in a graph and moving
towards different solutions is just exploring the graph. All kinds of graph transversal algorithms can be used then.
No idea what I'm talking about? No problem, it will all make sense at some point.

{% include video id="wGbuCyNpxIg" provider="youtube" %}

It's fundamental to understand that solving as many problems as you can and hoping to face a known problem during the interview is a terrible strategy.
There are so many different problems with so many different variations of them that even if you are lucky enough to face
a problem you have already seen, chances are that you won't remember the _"trick"_ to solve it.

Remembering tricks leads you nowhere. When the time comes, you are barely going to remember the solution. Or even worse, 
you will remember only half of it and are going to spend your energy trying to recall the missing details from your memory 
as you go. You will end up in a dead end. Your memory is only useful for remembering the patterns, not the individual problems.

When I say _patterns_ I'm not talking about the problem's categories. The following aren't patterns:
- Graphs transversals
- Dynamic programming
- Tree transversals
- Linked lists

Those are more like the general topics for the questions. The patterns are the techniques used for the solutions such as:
- Using a [sliding window](https://medium.com/leetCode-patterns/leetCode-pattern-2-sliding-windows-for-strings-e19af105316b) on an array (or a String, which is just an array of characters).
- Using [fast and slow pointers](https://en.wikipedia.org/wiki/Cycle_detection#:~:text=Floyd's%20cycle%2Dfinding%20algorithm%20is,The%20Tortoise%20and%20the%20Hare.) on a linked structure.
- Using [binary search to solve minimization problems](https://leetCode.com/discuss/general-discussion/786126/python-powerful-ultimate-binary-search-template-solved-many-problems).
- Using [multiple data-structures](https://leetCode.com/problems/lru-cache/) combined.

Once you understood the pattern you have a powerful tool in your belt for solving any problem similar to that one. Which is much more 
useful than just hard-coding a trick that won't last long in your memory.

# TODO-REDO-DONE

This was a game-changer for me which I discovered by pure serendipity. One day I had the crazy idea of re-doing an exercise 
I had previously solved. What a waste of time don't you think? If I solved the problem in the past, I would for sure be able
to do that again. In fact I should be able to solve it much quicker than before as I was already familiar with both problem
and solution.

Imagine my dissapointment when I couldn't figure it out. Ok, maybe it was just bad luck I thought. Let me try another one... same happened.
Was I getting dumber?

{:refdef: style="text-align: center;"}
![simpsons](/assets/images/acing-the-software-engineering-interview/simpsons.gif)
{: refdef}


Something had to change given that my approach wasn't working as I planned. I started analyzing my process for dealing with hard LeetCode problems.
Some problems are just really complicated and it's fine to check for the answer if you are not able to come up with an answer in a raesonable time frame.

No one has enough time to spend a week on one single problem which solution might be an [obscure algorithm](https://pablomusumeci.github.io/leetCode/count-bits/#brian-kernighans-algorithm).
Once of those that you either have knowledge of it or not. Only geniouses can come up with those algorithms (and probably not during an interview)
and I'm not one of them.

Checking the solution right away is also not the answer. You need to think hard for at least an hour or so. Hence, when you read and try
to understand the solution (sometimes just understanding the solution can take an hour on itself) it's more likely to stick in your brain. 

:warning: For the problems you *think you understand*, you must revisit them in the future to double-check
if you accurately understood them or not.

> There are known knowns. These are things we know that we know. There are known unknowns. That is to say, there are things that we know we don’t know. But there are also unknown unknowns. There are things we don’t know we don’t know.
>
> -- <cite>Donald Rumsfeld</cite>

This is the method I developed for fighting against the *unknown unknowns*. I call it **TODO-REDO-DONE**.

The first time you see a problem it's just something that belongs to your *TODO* list.
If you manage to solve it without breaking too much sweat then you can simply mark it as *DONE*.
What if this problem was a tough nut to crack? Maybe you even had to check the answer in the [discussion forum](#discussion-section-is-the-true-gold-mine).
Then it's better to reassess in the future if you truly understand all the details involved.
Let's move it to the *REDO* list and give it another look after a few days. Let it sink in.

> What I cannot create, I do not understand.
>
> -- <cite>Richard Feynmann</cite>

You will be exposed to fewer problems but the ones you have practiced you can be damn sure
that you understand them inside out. Less is more here.

Luckily LeetCode allows you to create your lists of problems so you can use that to keep track of
which state do they currently belong to.

{:refdef: style="text-align: center;"}
![TODO](/assets/images/acing-the-software-engineering-interview/todo-redo-done.png)
{: refdef}

# Walk before you can run

LeetCode problem's are classified in 3 levels of difficulty:

- ~~Easy~~ Puzzling
- ~~Medium~~ Mind-bending
- ~~Hard~~ Impossible

I started directly with Medium problems as this was not my first time preparing for interviews. I was expecting to
face Medium to Hard problems so I considered Easy ones to be unproductive for my preparation.

As I'm writing this text I'm thinking "How could I be so arrogant and stupid?". You live and you learn. Please do not repeat the same mistake
as I did. When you are just starting Easy problems are going to feel very challenging. Don't be dissappointed if you need an hour (or more)
to solve only one. 


I take for granted that you are not going to achieve the best solution. That is 100% guaranteed. Your solution is going to be
very crappy and inefficient but that's perfectly fine as you are going to check in the [discussion forum](#discussion-section-is-the-true-gold-mine)
why the performance of your idea is so bad.

Maybe your algorithm has the perfect time complexity and an implementation detail is trashing the performance at runtime (like for example concatenating lots of Strings in Java). 
No problem at all, now you know something new. Next time you won't repeat the same mistake.

Start with Easy and move to Medium when Easy problems start looking doable at first sight. 
I'm going to give you an example about why you should start by tackling Easy problems. 
It's not secret to anybody how binary search works. Can you code it in 2 minutes without hesitation?
Can you do it with enough confidence that you are not introducing any bugs? That's the level you want to achieve to succeed. 
Because binary-search is only going to be a tool you need to solve a bigger nastier problem. Same idea with other more complex algorithms such as BFS and DFS. 
You have to know them by heart, so when time comes you are not spending brain power on the **basic building blocks** but the big picture.

:warning: Beware of misclassification. Some Easy problems should be Medium and some Medium should be Hard. 
Don't be surprised if you find an Easy problem that's super tough to crack.

A small note about Hard problems. I haven't faced any at interviews and I think it makes sense as those problems 
are certainly [very hard](https://leetcode.com/problems/largest-rectangle-in-histogram/). They are extremly challenging even while practicing at home without any pressure whatsoever. 
I would say they are almost impossible to solve during an interview.

Solve the most famous ones like [N-Queens](https://leetCode.com/problems/n-queens/) or [Merge k sorted lists](https://leetCode.com/problems/merge-k-sorted-lists/) but don't obsess with them.
You might think that you are not ready for interviewing because you don't know how to solve one particular problem that
Google uses in their process. If have you reached that point chances are that you are going to be just fine.

# Practice every single day

Even if you don't have time for solving a full exercise. You can solve a problem across multiple 15 minutes sessions. Once you read
the description you will keep thinking about it in background mode.

[Build the habit](https://jamesclear.com/atomic-habits). The first few days are the hardest but it gets much easier with time. 
You will be surprised when you even start enjoying solving coding challenges. I'm not joking, it will happen to you if you practice enough. 
It becomes a tiny part of your life at least for a few months.

{:refdef: style="text-align: center;"}
![LeetCode meme](/assets/images/acing-the-software-engineering-interview/Leetcode-meme.jpeg)
{: refdef}

Think about it as a game. Some people solve candy crush levels, you do LeetCode challenges. Is not that different 
except that at the end you get the job of your dreams as a reward for playing.

Story continues in the [third part](https://pablomusumeci.github.io/acing-the-software-engineering-interview-part-iii/) of this [series of blog posts.](https://pablomusumeci.github.io/categories/#software-interviews)