---
title: Acing the software engineering interview - Part III
excerpt: FAANGtastic interviewing
last_modified_at: 2021-12-27
categories:
  - Software interviews  
tags:
  - Interviewing
toc: true
toc_label: Acing the SWE interview - Part III
toc_icon: code
toc_sticky: true
---


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