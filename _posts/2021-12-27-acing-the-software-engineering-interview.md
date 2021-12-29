---
title: Acing the software engineering interview
excerpt: FAANGtastic interviewing
last_modified_at: 2021-12-27
categories:
  - Software Engineering
tags:
  - Interviewing
  - Leetcode
toc: true
toc_label: Acing the SWE interview
toc_icon: code
toc_sticky: true
---

- Focus on coding interview first
- First barrier, most nervous about
X Solving problems in my own IDE, no timer
- Solved as many problems as I could. Maximized amount of problems solved.
- Gave up too quickly and check the solutions.
- My strategy was: Solve as much as you can, and if you are lucky you will face a problem you already solved at the interview and bingo.
- Doesn't scale. Leetcode has more than 2000 different problems. You cannot rely solely on your memory. 
- When the time comes, you are going to barely remember the solution. Or even worse, you remember half of it
try to recall the other half from your memory as you go and you end up stuck in a dead end.
- After a month, I realised that strategy was not going to work. I was making progress but very slowly.
- I tried re-doing exercises I've already done before and I couldn't solve them. How was that possible? Because I never
trully understood what I was doing.
- Listen to your interviewer, pick up the hints.
- start with easy

Some resources that really helped me:
- [System Design Interview – An insider's guide](https://www.amazon.com/System-Design-Interview-insiders-Second/dp/B08CMF2CQF) is a fantastic source of examples for preparing the SD interview. 
- An interviewer at FAANG recommended me the following course: [Grokking the system design interview](https://www.educative.io/courses/grokking-the-system-design-interview). I personally haven't used it but heard amazing things about it.
- A few YouTube channels that I recommend:
    - [SystemDesignInterview](https://www.youtube.com/c/SystemDesignInterview/)
    - [Code Karle](https://www.youtube.com/c/codeKarle)
    - [Gaurav Sen](https://www.youtube.com/channel/UCRPMAqdtSgd0Ipeef7iFsKw)
    - [Tech Dummies Narendra L](https://www.youtube.com/channel/UCn1XnDWhsLS5URXTi5wtFTA)
    - [Hussein Nasser](https://www.youtube.com/user/GISIGeometry)

My framework:
- Have 3 lists: To do, Re do, Done (state diagram excalidraw).
# First get the ball rolling

Before introducing the solution let me first present the problem. The way I started preparing for my coding interview
was suboptimal. Now I obviously see that but at that time it made sense as I needed to get the ball rolling somehow.

It takes courage to break status quo and start an endeavour to advance your career. You know that failing is not only
a possibility but it's likely to happen. The good thing is that you only have to succeed once to be succesful, you can (and you should) 
fail as many times as you want until you find that one company that you like and they like you.

Big tech is conservative for a good reason, they will only extend you an offer if they are pretty confident you are a fit for them.
It's a waste of time and resources to hire the wrong person for the job.

{% include video id="cQVFYVMhPlw" provider="youtube" %}

I promised to myself multiple times that I would start preparing for the interviews but nothing ever happened.
If you wait for the perfect setup then you are going to be waiting for a long time and maybe even forever.

So I got started on the path of least resistance using the tools I was familiar with. I created a project in my own IDE
and took some problems from the famous book [Cracking the coding interview](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/0984782850).
The problem with using my own IDE was that the IDE is really good. Seriously, modern IDEs are the training wheels of your bike.
Your IDE is so good (which is great for your day to day programming) that makes practicing hard as it helps you a lot without you even knowing.
You want to get back to basics.

Then you have the time factor. Is used for each problem as much time as I have or needed which quickly proved to match Parkinson's law:

> Work expands so as to fill the time available for its completion.
>
> -- <cite>Parkinson's law</cite>

I started using a stopwatch but you can always pause that to take breaks and resume afterwards. Or sometimes I even forgot that the thing
was running. I was measuring how long did it take for me to solve the challenge, but you want to do the other way around. You want
to set a time limit (like what happens during an interview) and then do as much as you can as fast you can.


I got frustated very quickly as I was trying to solve hard challenges from day one, which didn't help to keep my motivation high.
We all know how binary search works, that's not a secret. Go ahead and code it. Can you do it in 2 minutes without doubting 
and without introducing any bugs? That's the level you have to achieve in order to succeed. Because binary search is probably 
going to be one tool you need to solve a bigger problem. Same with other algorithms such as BFS and DFS. You have to know them by
heart so when time comes you are not spending brain power on the basic building blocks but on the big picture.


I was not enjoying the process and most important, I was not making progress at a good pace. It got me started which is crucial for
accomplishing any goal you might have but now after one month it was time for taking it to the next level. Something had to change.


# Leetcode
This was by far the single most useful tool I used during my preparation process, but in order to get the best out of it
you need to use it wisely. I will share some tips about how can you optimize your learning process, basically all the 
mistakes I made and you can avoid.

But first, why Leetcode?

## As real as it gets

Leetcode provides a plain text environment with no autocompletion (only syntax highlighting).
I have to admit it, my first time using Leetcode I couldn't even write a simple for-loop in Java. 
I was so depended on IntelliJ features that even the most simple syntax felt weird to type. 
It's what it is. This is how are you going to be evaluated, so better to be comfortable in that same kind of environment.

Your brain is so used to your IDE features that you don't even know you are using them until you don't have them anymore.
You have to learn the basics again. Debugger? Forget about it, here we think hard and use strategic prints to understand what's going on.

{:refdef: style="text-align: center;"}
![Blind](/assets/images/acing-the-software-engineering-interview/Blind.jpeg)
{: refdef}


You will have to know the APIs available in your language of choice. I became really comfortable using things I never used
at my job like `Arrays.deepToString` or doing bit-shifting operations.

⚠️ Your interviewer doesn't expect you to know absolutely everything. Everybody allowed me to google something if I needed to (of course you should
ask first if it's fine to do so).
Knowing these things by heart allows you to think so much faster as you don't need to 
worry about small details such as how do I print an `int[][]` or the API for defining a custom `Comparator`. 
Also, you have bigger problems to solve during the interview than fighting against the language you have chosen, 
so showing proficiency there definitely helps. Maybe it doesn't impress your interviewer that you know your language
inside out but it definitely provides a poor image if you have to google the basics.

## Mock assesments

This is a premium feature  but one that makes going premium definitely worth it. With this interviewing mode you get
some configurable amount of exercises and a fixed amount of time for solving them. 

{:refdef: style="text-align: center;"}
![assesment](/assets/images/acing-the-software-engineering-interview/assesment.png)
{: refdef}


Once you start there is no coming back. No pause, no bathroom break, no choosing the category or difficulty of the exercise. 
Just like a real interview would be. You want to expose yourself to thinking under pressure as much as possible. 
You can be a genious coming with elegant efficient solutions but if you can't do that on 30 minutes then you will fail the interview.

After time is finished, you get a report evaluating your performance against other candidates.

{:refdef: style="text-align: center;"}
![report](/assets/images/acing-the-software-engineering-interview/Leetcode-report.png)
{: refdef}

It also shows you an overview on the different areas you should focus for improvement.

{:refdef: style="text-align: center;"}
![overview](/assets/images/acing-the-software-engineering-interview/Leetcode-overview.png)
{: refdef}

:warning: Don't be distracted by those scores if you are doing this (and most people are) as preparation for interviewing.
The score is gauged against time complexity and memory usage but it doesn't take readability into account. Sometimes
the most efficient solution is the hardest to read, understand or debug. Your interviewer is evaluating you on those topics as well
even if they are not judged by the Leetcode reporter. That doesn't mean they will be satisfied with a brute-force solution that's 
readable, but I guess you get the point.

## Think and only then act

This is about impulse control. When you have been coding for 15 minutes and feel that you finished your algorithm, the immediate
urge is to hit the **RUN** button and expect to see that magic green text that says <span style="color:green">**SUCCESS**</span>. Don't.

Once you finish your code you need to review it again.

When you click **RUN** and you get a dissapointing <span style="color:red">**FAILURE**</span> result, 
you feel the urge to quickly fix the obvious (best case scenario) issue and hit run again. 

Most of the times, you will find that there was not only one error but many other hidden in your code waiting for this moment.
Every time something fails, take your time to analyze the problem. Not only the line that fail, but the entire code again. 
If you missed that one thing, how do you know that you haven't missed many others like that one?

{:refdef: style="text-align: center;"}
![Blind](/assets/images/acing-the-software-engineering-interview/stop-think-act.jpeg)
{: refdef}

Your interviewers are going to judge what kind of programmer you are:

- Are you someone who stops and calmly thinks if there is more than meets the eye? Someone that carefully checks again 
the code to understand what went wrong.

- Are you a hack-and-slash programmer? Someone who tries to duck tape the error adding another if statement, hitting run without
thinking and praying that this time all the test cases are green.

This is also a valuable advise for your career. Every time I send a pull-request I look at the same piece of code 
3 different times using 3 different diff tools. Most of the times I look at the code again
 I find something I've missed in the previous self-review round.

If I didn't control the urge to click **SUBMIT** and call it for the day, then I would be abusing my reviewer's time. 
They would have to flag all the issues that I could have fixed on my own if I had been a bit more careful and less impulsive.

## Free vs Premium

I started with a free subscription and I think everybody should start the same way. Free version is more than enough to
get you started. You can only take true advantage of the premium features once have solved a large amount of the basic easy problems the platforms provides.

After one month of using it 2 hours a day every single day (not exaggerating), I finally
decided to **invest** 35 USD (~30 euros) to get the best out of my time. 
I reasoned the cost was 1 euro per day which is close to nothing as I only planned to use it until I landed the job of my dreams.
Hopefully that was not going to take forever, but I had no pressure to change jobs quickly. My focus was on finding the
best opportunity for my career and in order to get an offer from those companies I to master my coding skills. Leetcode was
going to help me do that, and if Premium features improved my prepartion even a slightly bit then it was already worth it.

Premium give you access to features like (sorted by importance for me):
- Premium questions
- Select questions by company
- [Timed assesments](#timed-assesments)
- Sorting questions by frequency
- Autocompletion
- No wait time for submissions
- Official solutions
- Explore cards

Is it really neccesary? I guess not. Does it help a lot? Hell yeah! This is probably the investment with higest ROI your are going to
make in your life. 35 USD can seem like a lot or not depending on where do you live, but if those 35 USD help you landing a better job 
(and most likely a better offer that can potentially be thousands of dollars more per year) then it's a price worth paying.

## Discussion section is the true gold mine
After solving a problem (even with a terrible brute force solution) you **must** enter the discussion section of the challenge.
This is not optional if you ask me, here is where the magic happens.

In the discussion forum you will find that there were probably (at least) 3 complete different ways of getting to an answer. 

Each one with their own pros and cons. Probably the most performant solution is an already existing algorithm or obscure technique 
that no one can reallistically come up with it during an interview unless they've seen it beforehand.

That's fine, no expects you to do that anyway. But reading, thinking and understanding those solutions will expand your horizon about how problems 
can be solved. You most probably can use one of those ideas in another exercise because at some point [all the problems start to look similar to
another one you already solved](#leetcode-templates).

I tried to contribute to the discussion section as much as I could. Answering questions, upvoting good solutions and even posting my own solution.
Sometimes the core logic of my code was the same as another existing solution, but I considered posting like submitting a pull-request at work. 

Helped me to double-check my solution, add comments to the non straightforward parts of the code and also write a brief explanation of how the
algorithm works in plain english. I tried to use the [Feynmann technique](https://fs.blog/feynman-technique/) for diving deep into
my understanding of the solution. It happens to me more often that I would like to admit but I feel that I understood something... just to realize
that I cannot explain it in a simple way. Only then I see that I didn't fully get the idea *yet*.

> Now that you think you understand a topic reasonably well, explain it to a 12-year-old.
>
> -- <cite>The Feynman Technique.</cite>

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

I managed to finish the first exercise on time just to have a very similar situation with the second one. Simple challenge but screwing it due 
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
at the Leetcode discussion forums will provide a starting point for a solution.

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
was in our power, we studied for countless hours, we've done hundreds of Leetcode challenges. 
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

