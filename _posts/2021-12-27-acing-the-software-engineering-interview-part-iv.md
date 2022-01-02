---
title: Acing the software engineering interview - Part IV
excerpt: FAANGtastic interviewing
last_modified_at: 2021-12-27
categories:
  - Software Engineering
tags:
  - Interviewing
  - LeetCode
toc: true
toc_label: Acing the SWE interview
toc_icon: code
toc_sticky: true
---


# About coding interviews

## My journey

For the last three months I've been preparing myself for software interviews while also interviewing (ain't better preparation than real-world practice) hoping to find my dream job.
Took me lots of hard-work but I can gladly announce that I finally found it. It was an amazing experience that taught me a lot.
I not only learnt about programming but about enduring tough challenges and achieving what I considered almost impossible when I started.
I picked up how to prepare myself for performing under pressure like atlethes do. Become comfortable being uncomfortable.

I wanted to extensively describe my experience while my memories are still fresh and trustworthy. If this series of posts help at least one single person
I will be more than satisfied with the outcome. If I was able to accomplish my goal of landing my dream job then anybody can, I have absolutely no doubts about that.

It takes courage to break the status-quo and start an endeavor to advance your career. Specially if you are pretty comfortable at 
your current job as I was. It's a hard decision that you can delay forever but not without consequences.
You know that failing is not only a possibility but it's likely to happen. The good thing is that you only have to succeed once 
during your job search to be succesful. You can (and you should) [fail as many times](#exposure-therapy) as you want 
until you find that one company that likes you and you like them.

I had a very clear view on what I wanted as a next step (or at least that's what I thought at that time) for my career. I wanted to join [Big Tech](https://en.wikipedia.org/wiki/Big_Tech).
I knew I had to prepare myself really well If I wanted to have a real chance of getting a job at those companies. But how? 

> Every battle is won before it's ever fought.
>
> -- <cite>Sun Tzu</cite>

## Big Tech interviewing

First step was to discover how my skills were going to be judged so I could best prepare for those tests. 
Getting an offer from Big Tech is an extremly challenging undertaking. These are the largest tech companies where the smartest engineers work. Best of the best.
The problem for me is that Big Tech is really conservative and for a good reason. Those gigantic companies only extend offers if they 
are pretty confident the candidate is an absolute fit.


Interviewing for Big Tech is a lengthy process that can easily take from one to two months. You must pass a large number of different
interviews if you want to find the pot of gold at the end of the rainbow. The reason behind those many interviews is that companies strive for minimizing false positives (hiring the wrong person) 
at the expense of false negatives (not hiring the right person). It's a waste of time and resources for them to hire the wrong person for the job. You can argue that this is the case for every single company
but smaller companies are more willing to take bets on people. 

{:refdef: style="text-align: center;"}
![Interviewing chart](/assets/images/acing-the-software-engineering-interview/interviewing-chart.png)
{: refdef}

Getting your foot in the door is much harder than you think. Submiting your resume through a company's application portal has
very little chances of success. Don't be dissappointed if you never even receive an acknowledgement on your application. 
I strongly suggest you to leverage your network at this point. Getting a referral will guarantee you a first interview.
People will also be happy to refer you as they most surely get a big check for every person referred by them who gets hired.
Your brain will remark that if you don't pass the interviews your referral will think you are stupid. Don't listen to this message.
It's the part of your brain that loves the status quo. Go to that friend and ask for that referral, it's a win-win situation.


In this post I will focus on how to prepare yourself for the coding interviews. By *coding interview* I mean tipically 
a one hour session with one or two interviewers where you will be given one or two coding challenges to solve.
Your mission is to come up with an efficient algorithm to showcase your problem-solving skills aside from your technical abilities.
Not only you have to think about the solution, you have to explain out-loud what is your thinking process as you go. 

For the ones who have never experienced such interview, it's worth mentioning that what happens during that one hour session is 
unquestionably very far away from what we do at our current jobs. It's still programming of course, but everything else aside of that is just different.
I had a hard time explaining to my parents why I needed to prepare for months before interviewing for a job. Regardless of how much experience
you have as a software engineer you still have to go through a very thorough preparation process if you want to have a decent chance.

You can find more about Big Tech interviewing here 👇

{% include video id="cQVFYVMhPlw" provider="youtube" %}

## Does this make any sense?

I get it. Interviewing is a complete different skill.
Is it fair? Does it make sense? It's the game we have to play. Sometimes I wonder if companies do these crazy interviewing processes just to
see who has a will strong enough to endure all the preparation required. That might be the real test, a test of character.

StackOverflow's co-founder [Joel Spolsky mentions the following idea about hiring programmers](https://www.joelonsoftware.com/2006/10/25/the-guerrilla-guide-to-interviewing-version-30/):

> You’re looking for people who are smart and get things done.
>
> -- <cite>Joel Spolsky</cite>

The coding interview checks those boxes. That's why your interviewer will most likely clarify at the beginning of the session that
they want to see running code. No pseudo-code but actual code.

I also think that it's an extremely efficient process and to illustrate that I will now compare it against the other 
most used or suggested alternative on the market.

## Take-home assignments

Which other tools do companies have for evaluating a candidate's skills? A take-home assignment sounds like a reasonable thing to do.
You remove the stress and pressure for the candidate to think, code, and explain all at the same time. 

Specially when asking him to solve a kind of problem which is miles away from anything they have done during their entire career.
That's one of the reasons why people fresh out of university do better in coding interviews compared to more mature senior engineers.
If you took your CS courses a few months ago then it's more likely for you to remember how to write an in-order transversal on a binary
tree compared to someone who has been shipping production-quality software and providing operational support for the last five years.

{:refdef: style="text-align: center;"}
![Suppa](/assets/images/acing-the-software-engineering-interview/suppa-interview.jpeg)
{: refdef}

Knowledge assesment is only one aspect of interviewing someone. Companies realize that asking a candidate to invest 8 to 10 hours of their time 
on solving a problem at home is a lot. Most people can't even afford to do that as they have other commitments such as 
their current job or even more important than that: Their own family.

Even if the company states that "it should only take around 3 hours" we all know that everybody is going 
to spend much more time than that. We all want to show what we are capable of so putting some extra effort into it doesn't sound like a crazy idea.
Production-quality code is documented code with full (or at least a decent) test coverage.
No one wants to submit a crappy assignment as that would be the same as putting on your LinkedIn jobtitle "Subpar engineer".

This is also not the end of the story because then if the company was lucky enough to receive an assignment instead of being ghosted
by the candidate, then and only then company needs to find two reviewers (you don't want to rely on the biases of only one person, do you?).
Reviewers also have to put a fair amount of work into this. They must review the code, reason about the logic (you would be surprised about what candidates might submit) 
and write comments about the things they don't like as they have to provide feedback for the candidate.


Even if they are 100% sure it's a no-go after reading the first five lines of code, they still have to provide feedback.
It looks terrible if a candidate spent several hours working on 
your assignment and then you just email them a message saying only: <span style="color:red">**REJECTED**</span>.
You want your candidates to think positive about your company even if they cannot meet the quality bar yet. They might
apply again in the future or talk about their experience at your company with their coleagues. You want them to love your company.

Overall the process is much slower due its async nature. The candidate needs to find a moment of their time where they 
can afford to spend some consecutive hours focusing on the task which will probably happen during the weekend. 
Then reviewers need to find a moment on their week to stop doing any other task and review the code (which might happen at different times for the different reviewers). 
Then they need to come together to agree on a yay/nay decision. And only then the recruiter can decide to move forward or not
attaching the given feedback.

Now compare this approach against a one-hour synchronous session between candidates and interviewers. Sessions where not only the candidate's skills 
can be assesed (maybe suboptimally) but also their communication style and interpersonal skills.

Pros:
- Better assessment of candidate skills on an scenario closer to the real work environment
- Requires less preparation for the candidate
- Suitable for good engineers who fail to perform in an unrealistic high pressure situation

Cons:
- Takes more time for the candidate to complete (without considering prep time)
- Takes more time for the interviewers to review
- Interviewers can only review real code properly in the technologies they are profficient at
- Overall slower due to synchronization overhead
- It's impossible to asses soft-skills
- It's easier to cheat

See? Companies are not evil, they just care for efficiency. This is not a silver bullet and I'm not against assingments, 
but after doing this extensive comparision I find coding interviews as a reasonable trade-off to make.

## Never let perfect be the enemy of good

I had promised myself multiple times that I would start preparing for the interviews right away but that never happened.
If you wait until you find the perfect setup then you are going to be waiting for a long time.
The way I started preparing for my coding interview was suboptimal but I needed to stop procrastinating and start somehow.

To begin with I started on the path of least resistance using the tools I was already comfortable with. I created a project inside my own IDE
and used some random problems from the famous book [Cracking the coding interview](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/0984782850).
The downside of using my IDE is that modern IDEs are amazing pieces of software.
Your IDE is so freaking good (which is great for your overall efficiency at normal circumstances) that makes practicing quite hard 
as it helps you a lot more than you know. You want to get back to basics.

After that, I had to start considering the time factor. I initially allocated for each problem as much time as I had or needed for figuring out an answer. 
This approach quickly confirmed Parkinson's law:

> Work expands so as to fill the time available for its completion.
>
> -- <cite>Parkinson's law</cite>

Then I started using a stopwatch. However, you can always pause it to take breaks and resume afterwards. Sometimes I even forgot that the thing
was running at all. I was measuring how long it took me to solve a single problem where what you are actually after is how much progress you can achieve in a fixed amount of time.
You want to [set a time limit](#mock-assessments) (like what happens during interviews) and then do as much as you can as fast you can inside that time frame.


The next difficulty were the problems I had choosen to practice against. [Cracking the coding interview](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/0984782850)
contains 189 programming questions which are not the easiest ones to start with.
Frustration arised very quickly as I was trying to [solve Hard problems from day one](#walk-before-you-can-run). 

I was not enjoying the process and most importantly, I was not making progress at good speed. It got me started which is crucial for
accomplishing any goal. Now after one month it was time for taking it to the next level. Something had to change.


# LeetCode
By far the single most valuable tool I used during the entire preparation process. Works great out of the box but if you want to get
he best out of it you need to use it wisely. Optimizing your learning process is key for fast improvement. Learn how to learn.

But first, why LeetCode?

## As real as it gets

LeetCode provides a plain text environment with no autocompletion (only syntax highlighting).
I have to admit it, my first time using the platform I couldn't even write a simple for-loop in Java. 
Typing even the most simple syntax without autocompletion felt so unnatural.
It's what it is. No secret here, you need to get used to it. This is how you are going to be evaluated 
so better to be comfortable in that same kind of environment.

Your brain is so used to using the IDE features that you don't even know you are using them until you don't have them anymore.
You have to learn the basics again. Using breakpoints? Forget about it, here we think hard and use strategic prints to understand what's going on.

{:refdef: style="text-align: center;"}
![Blind](/assets/images/acing-the-software-engineering-interview/Blind.jpeg)
{: refdef}


You will have to know the APIs available in your language of choice. I became genuinely comfortable using things I had never used
at my job like `Arrays.deepToString` or doing bit-shifting operations. It was unnatural until it wasn't.

⚠️ Your interviewer doesn't expect you to know absolutely everything by heart. Everybody allowed me to google something if needed.
Of course you should ask them first if it's acceptable to do so.
Knowing APIs by heart allows you to think so much faster as you don't need to 
worry about details such as how to print an `int[][]` or the syntax for defining a custom `Comparator`. 
You have larger problems to solve during the interview than fighting against the language you have chosen. 
Showing proficiency there definitely helps. Maybe it doesn't impress your interviewer that you know your language
inside out but it projects a poor image of yourself if you have to google the basics.

## Mock assessments

It's a premium feature but one that makes going premium definitely worth it. With this _interviewing mode_ you get
a configurable amount of random exercises to solve in a fixed amount of time.

{:refdef: style="text-align: center;"}
![assesment](/assets/images/acing-the-software-engineering-interview/assesment.png)
{: refdef}


Once you click the start button, there is no coming back. No pause, no bathroom break, no choosing the category or difficulty of the problems. 
Exactly as real interview would be. You want to [expose yourself](#exposure-therapy) to thinking under pressure as much as possible. 
You can be a genius who designs elegant solutions but if you can't do that in 30 minutes then you will most 
likely fail.

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

## Think and only then act

Impulse control is everything. When you have been coding non-stop for 15 minutes and feel that you've finished your algorithm, the immediate
urge is to hit the **RUN** button and hope to see that magic text saying <span style="color:green">**SUCCESS**</span>. Don't.

Once you've finished your coding you need to review the changes. Then review them again.

If you click **RUN** and get a dissappointing <span style="color:red">**FAILURE**</span> result, 
you will feel the natural urge of immediately fixing the obvious (best case scenario) bug and submitting again as fast as possible. 

I'm not a fortune-teller but I'm quite confident that regularly you will find many other bugs were hidding in your code 
waiting for their chance to suckerpunch you.
When something fails, take your time to analyze the problem and understand what happened. Not only the line that failed but the entire code again. 
If you missed that one single tiny thing, how can you be sure that you haven't missed many others more?

{:refdef: style="text-align: center;"}
![stop-think-act](/assets/images/acing-the-software-engineering-interview/stop-think-act.jpeg)
{: refdef}

Your interviewers are going to judge what kind of programmer you are:

- Are you someone who stops to calmly think if there is more than meets the eye? Someone that carefully checks the code 
to understand what went wrong.

- Are you a hack-and-slash programmer? Someone who tries to duck tape the error by adding yet another if statement, submitting without
thinking and praying that this time all the test cases are 💚.

This is also valuable advice for your career. Every time I have to send a pull-request, I look at the same piece of code 
three different times using three different diff tools. More often than I would like to admit, I end up finding something 
I've missed in the previous self-review round.

If you don't restrain that urge of clicking **SUBMIT** and calling it for the day then you are abusing your reviewer's time.
They will have to flag all the issues that you could have fixed on your own if you had been a little bit more careful with your work.

## Free vs Premium

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

## Discussion section is the true gold mine
After solving a problem (even through a terrible brute force solution) you **must** enter the discussion forum.
Doing that is not optional because there is where the magic happens.

In the discussion forum you will find that there were probably (at least) three complete different ways of solving the problem.
Different solutions with different trade-offs in terms of time and space complexity.
Probably the most performant solution is an already existing algorithm or obscure technique that no one 
can realistically come up with it during an interview unless they've seen it beforehand.
That's fine as no-one expects you to come up with such during an interview anyway. 

Nonetheless, reading and thinking about those solutions will expand your horizon about how problems can be solved. 
Those ideas can be leveraged in other problems because at some point [all problems start to look similar to one you previously solved](#leetcode-templates).

I contributed to the discussion section as much as I could. Replying to questions, upvoting the best solutions and even posting my own.
Sometimes the core logic of my code was the same as another solution but I considered posting like submitting a pull-request at work.

It helped me to double-check my work and add comments to the non-straightforward parts of the code. Also forced myself to write a brief explanation of 
how the algorithm works in plain English. I use the [Feynmann technique](https://fs.blog/feynman-technique/) for diving deep into
my understanding of the solution. Sometimes I feel that I finally understood something and still I felt incapable of explaining it clearly.
That's a reality check where I come clean with myself about how much of the topic do I actually comprehend.

> Now that you think you understand a topic reasonably well, explain it to a 12-year-old.
>
> -- <cite>The Feynman Technique.</cite>

## LeetCode templates
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

## TODO-REDO-DONE

This was a game-changer for me discovered by pure serendipity. One day I had the crazy idea of re-doing an exercise 
I had previously solved. What a waste of time don't you think? If I solved the problem in the past, I would for sure be able
to do that again. In fact I should be able to solve it much quicker than before as I was already familiar with both problem
and solution.

Imagine my dissapointment when I couldn't figure it out. Ok, maybe it was just bad luck I thought. Let me try another one... same.
Am I getting dumber?

{:refdef: style="text-align: center;"}
![simpsons](/assets/images/acing-the-software-engineering-interview/simpsons.gif)
{: refdef}


Something had to change given that my approach wasn't working as I planned. I started analyzing my process for dealing with hard LeetCode problems.
Some problems are just really complicated and it's fine to check for the answer if you are not able to solve it in a resonable time frame.

No one has enough time to spend a week on one single problem which solution might be an [obscure algorithm](https://pablomusumeci.github.io/leetCode/count-bits/#brian-kernighans-algorithm).
Once of those that you either have knowledge of it or not. Only geniouses can come up with those algorithms by themselves (and probably not during an interview)
and I'm not one of them.

Checking the solution right away is also not the answer. You need to think hard for at least an hour or so. Hence, when you read and try
to understand the solution (sometimes just understanding the solution can take an hour on itself) it's more likely to stick in your brain. 

:warning: For the problems you *think you understand*, you mustrevisit them in the future to double-check
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

## Walk before you can run

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
No problem at all, now you know something new. Next time you are not going to repeat the same mistake.

Start with Easy and move to Medium when Easy problems look doable at first sight. 

To give you an example, it's not secret to anybody how binary search works. Can you code it in 2 minutes without doubting?
Can you do it confidently without introducing any bugs? That's the level you want to achieve to succeed. 
Because binary-search is only going to be a tool you need to solve a bigger nastier problem. Same idea with other more complex algorithms such as BFS and DFS. 
You have to know them by heart, so when time comes you are not spending brain power on the **basic building blocks** but the big picture.

:warning: Beware of misclassification. Some Easy problems should be Medium and some Medium should be Hard. 
Don't be surprised if you find an Easy problem that's super tough to crack.

A small note about Hard problems. I haven't faced any at interviews and I think it makes sense as those problems 
are certainly very hard. They are extremly challenging even while practicing at home without any pressure whatsoever. 
I would say they are almost impossible to solve during an interview.

Solve the most famous ones like [N-Queens](https://leetCode.com/problems/n-queens/) or [Merge k sorted lists](https://leetCode.com/problems/merge-k-sorted-lists/) but don't obsess with them.
You might think that you are not ready for interviewing because you don't know how to solve one particular problem that
Google uses in their process. If have you reached that point chances are that you are going to be just fine.

# You are your worst enemy

## Screwing up my first big chance

After practicing for 2 months, I had my first interview with FAANG. I didn't feel ready at all but I don't think you will ever feel ready for this.
I had 45 minutes to solve 2 **VERY SIMPLE** code challenges. I came to the interview expecting something crazy and impossible to solve, but when
I saw that the first question was some simple recursion over a binary tree plus some simple math over the values I felt relieved. I was able to pass this interview.
My dream of FAANG was not impossible. This was just the first step but I felt confident on my skills to overcome this obstacle.


Motivated by this realization, I jumped into coding immediately as I knew that I've solved a problem very similar problem to this one a few days ago. 
After coding my first solution in a few minutes, we started testing and debugging with the interviewer only to find out that my code was very buggy.

I didn't consider some (or most) of the edge cases and then got really nervous. As I was fixing the bugs with some hints from my interviewer my 
confidence started to go down. Here I was, facing a really easy problem and blowing away this opportunity. I felt terrible. I was expecting
to fail solving a hard-challenge that I was not smart enough to figure out, but I wasn't prepared to fail a simple challenge just because I was
too nervous. Maybe I'm not as good as I thought or I was not prepared as much as I hoped.

If this was already not bad enough, when we started talking about time complexity I just said something **OBVIOUSLY WRONG**. My mind 
was silently saying to me:

> Bye bye opportunity at FAANG. Congratulations Pablo for screwing it up big time.
>
> -- <cite>Pablo's brain during the interview.</cite>

I managed to finish the first exercise on time only to have a very similar situation with the next one. Simple challenge but screwing it due 
to being really nervous and not thinking clearly.

## Back to the drawing board

Failing this interview was the best thing that could have happened to me. I got an important lesson out of it. 
I had to think before acting. I knew that I had to do this, is not rocket science but anyway failed to restrain the impulse of coding right away.
I failed to be calmed and concious. It's something very easy to say but very hard to accomplish during the heat of the moment.

I decided to follow the same approach as for the technical preparation. I was going to study and practice how to keep myself calmed and focused during  intense 
periods of stress.
I knew I was definitely not the first person to experience this, everybody gets nervous if being observed during coding. It's not something we
do on our job. The entire interview situation (coding a complex algorithm you never used at work in a plain text editor without autocompletion 
while you are being observed by someone judging everything you say and every line of code you write... all that in 50 minutes) is something
our brain is not familiar with, which makes being relaxed nearly impossible due to the lack of familiarity with the situation.

## REACTO

No, this is not yet another Javascript library. This is the secret I found for keeping a cool head and show my A-game during the interviews.

**REACTO** stands for:
- **R**epeat
- **E**xamples
- **A**pproach
- **C**ode
- **T**est
- **O**ptimize

I sticked a post-it note to my desk, and every time an interview started I looked at it to remind myself how should I proceed.
Regardless of how simple or complex the challenge was, I religiously followed the same approach over and over. I turned out great for me. 

[Go ahead and read the full post here](https://www.fullstackacademy.com/blog/how-to-ace-a-technical-interview-reacto).

### Why REACTO works?

Repeating the problem like a parrot to you interviewer will buy your brain enough time to start some background processing.
You might think at first that you are just wasting precious time you could be using for coding, but coding only takes a few minutes if you know
exaclty what you the code should be doing.

Once you repeated the question to your interviewer, you now understand a tiny bit better what the problem is about. 
But you have only scratched the surface, now it's time to go deeper into the problem space (not yet the solution space).

The interviewer will probably give you an example of the input/output expected to be handled by whatever algorithm you come up with. 
Use this to understand what the problem is about, this is a perfect opportunity for thinking about edge cases. 
Ask questions such as "What should be the output if the input is **${UGLY EDGE CASE}**?".

Remember that your brain is still running that background thread which is trying to answer the question that lies in front of you.

> How the heck I'm I going to solve this problem?
>
> -- <cite>Your brain in background mode</cite>

You need to keep buying your brain time, trusting that all those exercises you practiced before the interview and all the hours spent 
at the LeetCode discussion forums will provide a starting point for a solution.

{% include video id="DIR_rxusO8Q" provider="youtube" %}

Now we enter into the approach section. Your brain already had like 5 minutes of processing to come up with something. 
Something can be a brute force solution, that's a perfectly valid start. Still better than nothing. 

Communicate this to your interviewer so they know what you have in mind, both the solution you found 
and why you don't particularly like it as you think that this problem can be solved
in a more efficient way. Feel free to mention the time complexity of the ugly solution. 
Providing this data is an extra point for you as you know how to measure how bad is the bad solution.

Ask them if they want you to code this bruteforce solution or better to spend time thinking about better alternatives.

This dialog is really important for your interviewer. They know you have something in mind and you understand the limitations of that.

Now it's the time for having an open discussion (both with yourself and with the interviewer) about trade-offs, bottlenecks, 
and what is the part of your algorithm that should be improved to achieve a better time complexity.

Agree with your interviewer on the approach you plan to take before writing any code whatsoever. This is the best usage of your time. 
Once that the approach was discussed and agreed, then it's time for coding. 

So far, you have spent around 5-10 minutes with your interviewer doing things which are everything but coding. 
Once you start coding is harder (not impossible) to go back and design a completely different solution.
Because you already spent the time trying to make an idea work, because your mind is fixated on the things you already wrote and forcing that
piece of code to be the solution. 

It's not impossible to go back and discuss a new approach but time is ticking, so better to use time
at the beginning to maximize the chances of getting the right approach on the first try.

Last but not least, once coding is done time for adding tests. You probably don't need to run these but good to show
what kind of tests would you write. Try to come with as many edge cases as you can.

## Exposure therapy

One way of overcoming you fear and anxiety of interviewing is getting used to them. Interviewing is something we rarely do. You might
have a few interviews every couple of years, but the next time you are interviewing again you probably forgot how it felt. 
The fact that we do them very sparsely over the years doesn't help us to get familiar with the feeling. Also, no one likes being judged.
So even if you go through a thousand interviews you will always get nervous, but I can guarantee you that how you feel on interview number 3
compared to interview number 47 differs on a few orders of magnitude.

The way I dealt with this situation was some sort of [exposure therapy](https://www.apa.org/ptsd-guideline/patients-and-families/exposure-therapy). I forced
myself to interview as much as I could for a number of reasons. Every interview you endure makes you feel a bit more used to the situation.
You become a tiny bit stronger regardless of the outcome. 

{:refdef: style="text-align: center;"}
![Fear](/assets/images/acing-the-software-engineering-interview/fear-practice.png)
{: refdef}


Another benefit from going into an interviewing marathon is that your chances of landing a good job increase significatively.
When the pool of companies you are interviewing is larger, then your chances of landing a better job also get larger. A better job means a better job for you. 
This is doesn't mean necessarily more money. There are multiple reasons why a job is better for you than any other and those reasons are different for each one of us.
Can be more money, more career opportunities, a more comfortable environment, etc.

And this also works for the money side of things. Competing offers give you leverage to negotiate a better deal. 
There are more companies that want you to work for them, they need to bring their best offer to the table to get you. 
Supply and demand, as simple as that. **If you want a good offer you have to earn it**. How? Interviewing a lot.

## Be in the zone

### Preshot routine

Have you ever noticed how each basketball player has a different ritual or routine before shooting a free throw? Why do they do it?
Do they think it brings them luck? Are all of them superticious? Not at all.

There are [studies](https://pubmed.ncbi.nlm.nih.gov/2928064/) about how the preshot routine improves shooting percentages.

> A significantly larger number of baskets were made in the preshot routine condition than without the routine.
>
> -- <cite>Effects of preshot routine on free-throw shooting</cite>

{:refdef: style="text-align: center;"}
![Lebron](/assets/images/acing-the-software-engineering-interview/Lebron.gif)
{: refdef}

### Why does a preshot routine work?

A free-throw is the most simple shot of the game if you think about it. You have all the time in the world and no defenders to block you.

But that can also be a problem, you are taking the shot alone... but you are there alone with your own thoughts.

When you focus on your preshot routine, your free-throw becomes a very similar shot as the ones you take during practice. You are not thinking about
the pressure of the game, you are not thinking about the fear of missing, you are just there focusing on the same repetitive routine you've done hundreds of times.

### How does this apply to me?

We are not basketball players, but we can benefit from taking our mind to a comfortable place before an stresful interview. We already did everything that 
was in our power, we studied for countless hours, we've done hundreds of LeetCode challenges. 
There is very little we can get by studying until the very last minute before the interview.

It's better to use that time to relax (easy to say hard to do) so we can give our best performance during the interview. 
Trust your preparation, trust yourself.

My pre-interview routine started 20 minutes before showtime. I prepared my desk, served myself a tea and a glass of water.
Then, once my environment was ready I put on my noice cancelling headphones and listened to one particular song. Always the same song.
But I didn't listen to the song while doing something else, that wouldn't have prevented my mind from getting nervous about what's was coming next. 
I sit and watched the entire video-clip with my full attention, no discractions allowed. 
Like a child watching the same movie over and over, I turned off the world entirely, put my phone in airplane mode 
while sitting on the same chair with the same setup as always.
Set the videoclip in full screen mode and observed every little detail of it while keeping my mind blank. Being in the moment.

I recommend choosing a song you love and particularly one that **energizes** you. I recommend rap (Eminem is a great choice) 
but that's up to you, go and find your own ritual.

You want something that makes you enter the interview like Michael Jordan entering  
a play-off game, ready to excel.    [Listening to the Chicago Bulls song from Alan Parsons still gives me goosebumps](https://www.youtube.com/watch?v=Zn6kiimEsYc).

{:refdef: style="text-align: center;"}
![MJ](/assets/images/acing-the-software-engineering-interview/Michael-Jordan-Clapping.gif)
{: refdef}

Maybe this doesn't apply to you or you are a master of keeping your nerves under control, but after my first bad experience with FAANG I was
open to try anything that calmed me down so I could show everything I knew when it was most important. 
I think this topic is as important (maybe even more) as the technical preparation. 
If you know everything but you cannot demostrate that to your interviewer, then the outcome will be the same as if you hadn't practiced at all.

By the way, I received an email 3 weeks after the interview congratulating me for moving into the next stage. I was quite confident
that I was going to fail but I got another chance. I took this as a free pass that helped me to keep interviewing with this FAANG company
more relaxed. I had nothing to loose, and that mentality helped me to better perform in what was coming next.

## Show time

Everything that happened before this point was just preparation. We've done our homework, we practiced a lot,
we executed our ritual to put our mind into a known happy place. Now it's showtime.

We know how this is going to be because we have done it many times already. We have a post-it in our desk
reminding us about the [REACTO approach](#REACTO). Now we need to go with the flow but things will
not be exactly the same as in our practice sessions. There is now a human (or maybe two) on the other side
listening to everything we say.

### Have a dialog

Sadly (or maybe luckily) interviewers cannot read our minds, their only input is what we say and what we code. 
And because we don't want to code things we haven't agreed with them, 
we need to start talking. I always love to start the interview by 
saying something like "I'm going to start thinking outloud now so I will probably say things that are absolutely wrong".

Remember that if they do their job correctly, your interviewer is there to make you shine. Their job is
to help you to perform at your highest level. They should be trying to calm you down, even play some jokes
to break the tension in the air.

The best interviews I ever had never actually felt like an interview. It was just me and a random person I've
never met talking about algorithms, data-structures and code in a very relaxed environment.

I think it's perfectly fine to ask things like: 

- "What do you think about this approach?"
- "Where do you think the bug might be?"
- "I don't like this part of the solution, do you have any idea about how can we improve this?"

But beware, even if it looks like a friendly co-op exercise they are still evaluating everything you say and do. So don't pull to hard.
They are there to help you but you must do the heavy-lifting. If you request too many hints or ask too many question then
it's a bad sign for them as you are not autonomous enough and you require more handholding than they would like to.

### Pick up the hints

During the interview it's extremely common that at some point if you are a bit stuck, the interviewer
is going to let slip some sort of hint to help you move forward. They are never going to say "do this" but they have already
seen a thousand different ways of solving this same problem on previous interviews. So if they suggest you something,
they are very likely trying to nudge you into a particular direction for a good reason.

Listen to them, they want you to succeed. Your first instict is (sadly) going to be something like "They are trying to
make me fall into a trap by suggesting the wrong approach. This is just another test!". It's a possibility indeed, 
but very unlikely. I would suggest you to explore the path they are showing you. Remember, they want you to succeed.

I also been on the other side of the table and I know how frustrating it's to see a candidate struggling,
throwing them a hint and them being unreceptive to other points of view. I know it's hard to open your mind
and actually to what the other person is saying, specially during periods of high stress where your brain CPU is 
busy working at 100% capacity to crack this problem.

{:refdef: style="text-align: center;"}
![Brain](/assets/images/acing-the-software-engineering-interview/brain.jpeg)
{: refdef}

You want to work with people whom are open to ideas that are not their own. So picking up the hint is good 
for you due to two very different reasons:

- Allows you to move forward towards a solution.
- Shows that you are someone who listens to their peers and is open to new ideas.