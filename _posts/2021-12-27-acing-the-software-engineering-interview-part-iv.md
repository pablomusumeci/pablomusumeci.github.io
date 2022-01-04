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

This is the fourth in a [series of blog posts](https://pablomusumeci.github.io/categories/#software-interviews) 
where I describe my interviewing experience and thoughts in detail.

Once you've passed the coding interviews, there are still two more interviews to come.
I think that the coding interview is the hardest and the one that requires the most preparation but
you needed to be succesful at all of them if you want to get your dream job.

# System design

This interview is mostly about designing high level components (boxes and arrows) for solving a particular scenario described by the interviewer.
The amount of things that can be discussed are pretty much endless, so your interviewer will guide you through the
areas they consider most important to be discussed. 

System design interviews can touch a bit of every topic.
Some people do more emphasis on the type of database used while some others care more about designing a clean API.

- Understand the CAP theorem
- Consistent hashing and its applications
- Different levels of consistency and their trade-offs
- Different database types and when to use which
- Sharding and replication
- Publish-subscribe pattern
- [API versioning](https://stripe.com/blog/api-versioning)
- Websockets and RPC

{% include video id="aXD4tWbkoJo" provider="youtube" %}

There is no bad or good solution, it all depends on the problem you are trying to solve and the trade-offs you are
willing to make. You might prefer availability over consistency when calculating the amount of likes on a social
media post. There it's not a big deal if you show incorrect (as in stale) data for a while as long as you show *something*.

But in systems where money is handeled we are generally more worried about strong consistency (calculating the right value)
at the expense of some downtime.

## Avoid naming names

I highly encourage you to avoid naming specific technologies and just stay with the most generic abstraction as possible.
Instead of saying "I would cache things in Redis", just say that you would use an in-memory datastore. 
I would use a NoSQL database in place of "I would use MongoDB". 

The moment you put a name out there your interviewers are going to start asking questions about that specific technology.
So restrain yourself from mentioning technologies you are not to familiar with. For this kind of situations I always say 
something like:

> Disclaimer, I've never worked with this technology but I read that **${BUZZWORD}** is generally used to solve this kind of problem.
>
> -- <cite>Pablo</cite>

You should at least know some of the very basics of **${BUZZWORD}** technology. Why do people recommend that for solving the problem?
Don't just talk for the sake of talking. Interviewers prefer to work with someone who admits when they don't know something
instead of bullshiting their way out of a situation.

## Resources 
- [System Design Interview – An insider's guide](https://www.amazon.com/System-Design-Interview-insiders-Second/dp/B08CMF2CQF) is a fantastic source of 
examples for preparing the SD interview. If you don't know how to start, please start with this book.

{:refdef: style="text-align: center;"}
![system design book](/assets/images/acing-the-software-engineering-interview/system-design-book.jpg)
{: refdef}

- An interviewer from *FAANG* recommended me the following course [Grokking the system design interview](https://www.educative.io/courses/grokking-the-system-design-interview). I personally haven't used it but heard amazing things about it.

I also wanted to share a few YouTube channels that I used:
   - [Hussein Nasser](https://www.youtube.com/user/GISIGeometry)
   - [Gaurav Sen](https://www.youtube.com/channel/UCRPMAqdtSgd0Ipeef7iFsKw)
   - [Code Karle](https://www.youtube.com/c/codeKarle)
   - [Tech Dummies Narendra L](https://www.youtube.com/channel/UCn1XnDWhsLS5URXTi5wtFTA)
   - [SystemDesignInterview](https://www.youtube.com/c/SystemDesignInterview/)


Also some blogposts I liked:
- [How Discord Stores Billions of Messages](https://blog.discord.com/how-discord-stores-billions-of-messages-7fa6ec7ee4c7)
- [Sharding & IDs at Instagram](https://instagram-engineering.com/sharding-ids-at-instagram-1cf5a71e5a5c)

# Behavioral interview

I always disregarded the soft-skills interview as I consider myself very talkative person. The stereotypical programmer
is introverted, socially awkward and highly intellectual. I recognize parts of me that match the standard nerd although
I always considered myself *normal* enough to pass *the psycopath test*.

{:refdef: style="text-align: center;"}
![standard nerds](/assets/images/acing-the-software-engineering-interview/standard-nerds.gif)
{: refdef}

At big companies, this interview is much more than just a check to ensure that you are not a wacko.
Behavioral interviews are there to check if you are a match for the company's culture.
A company's culture is not composed by their free lunch, parties and games rooms. 
The culture of a company is its DNA.


## What is the purpose of this interview?

I'm not going to go too deep into what embodies a company's culture but I will summarize it in a quote extracted from this [blog post I really like](https://camillaboyer.medium.com/why-cultures-fail-3151e72d3ca8).

> Culture is how we do things here and how people act when nobody is watching.

Interviewers will throw at you **open-ended questions** about your past experiences to understand who are you. 
Why? Because stories are a medium that more truthfuly reflect our core values compared to just describing our strenghts and weaknesses.
Stories teach. Let the story speak to the interviewer in its own way and skip the need to tell them what to think.
An example of a situation where you exhibited a particular trait is much more convincing than an empty statement about your persona.

All these questions start with something similar to  "Tell me about a time where..."

- You received tough feedback
- You had to provide tough feedback
- You built out a process
- You made a mistake
- You proposed an idea and was not agreed on
- You convinced someone to change their mind
- Your project failed
- You didn't have enough resources but still had to deliver a project

How should we approach those types of questions?

## What makes a good story?

This interview is all about telling a good story. We humans are fascinated by stories, 
that's the reason why we love watching movies and reading books.
Interviewers want to know who are you and the window through which they are going to look at your experiences is the story you tell them.
It's absolutely critical that you pick good stories to illustrate your past experiences.

A good story is not one that depicts you as the perfect person or employee. Think about it, would you like
to see a movie where the main character is flawless? That would be pretty boring.

The heroes we love are fragile and flawed. They make mistakes and not always win. What we love about them is 
that each failure allows them to emerge stronger than before.

> We do not learn from experience, we learn from reflecting on experience.
>
> -- <cite>John Dewey</cite>

It's natural to try hiding your weaknesses during interviews but you shouldn't. Self-reflection
shows a person that wants to improve. You know you are not perfect, you know there are areas you should improve but you are a work in progress.

You should carefuly prepare and pick the stories you are going to be using during the interview. Think hard about all
your previous experiences because picking the right story to tell is not an easy task. You want to select a story
that makes you look good but not perfect.

Think about stories where you...

- Demostrated initiative instead of just complaining.
- Took risks but without being reckless.
- Made a mistake while trying to do something with good intentions.
- Led by example and inspired others.
- Decided something that seemed right at the moment but ended up being the wrong call.

You might come up with a few potential stories that can answer each question. Select the ones that 
best showcase the reasons why you should be hired.

## A good story needs only a good storyteller

Now that you have a few candidate stories, it's time to write a script. You want to narrate the situation providing
enough context but without going to deep into unnecesary details. 

Some people suggest using the [STAR](https://www.themuse.com/advice/star-interview-method) method.

- **S**ituation
- **T**ask
- **A**ction
- **R**esult

I rather use an old time classic like the [three act structure](https://en.wikipedia.org/wiki/Three-act_structure).
Such construction is used in every single good story ever told. Setup, confrontation, and resolution.

{:refdef: style="text-align: center;"}
![heroes journey](/assets/images/acing-the-software-engineering-interview/heroes-journey.png)
{: refdef}

Now is where the fun beings. Use a friend to practice your story-telling. Just explain them the situation in around five minutes.
Request them to ask questions if something is not clear. You need to get rid of the plot-holes.
Telling the same story over and over helps you master how that particular story should be told. 
Think about the best stories you share together with your friends or that story your grandpa always brings up at family reunions.
Keeping a good pace is key. You want to speak slow enough so that the story is easily absorbed but not so slowly that the listener mind checks out of the room.


## What is the cost of lies?

> Every lie we tell incurs a debt to the truth. Sooner or later, that debt is paid.
>
> -- <cite>Chernobyl, HBO</cite>

You might think that you don't have any good stories to tell, that nothing trully remarkable or extrordinary happened to you at work.
Perhaps you are considering inventing a story that shows you have all the ingredients the interviewer is looking after in a candidate.

I'm going to tell you why that's a terrible idea. By doing this you are showing your interviewers a big fat red flag.
Interviewers are pros. They had this interview hundreds of times before. They know how a good answer looks like and they can smell
a false story from miles away.

There will be two or tree nested questions. It will be impossible for you to maintain a credible lie.
They will caught you red-handed and that's the worst possible outcome of the interview. Dishonesty is 
instant disqualification.

{:refdef: style="text-align: center;"}
![disqualified](/assets/images/acing-the-software-engineering-interview/disqualified.gif)
{: refdef}

Lying doesn't benefit you nor the company. You can only thrive in a work-place where you are a happy camper.
If you are not a mutual match then trying to force the relationship through lies will manifest later on.


## The Miranda warning

If you are at this interviewing stage, you probably wrote your resume a few months ago and completely forgot everything mentioned there.
You most likely bent the truth a little bit to make your resume more attractive to recruiters, no one pays attention to everything
that's written there anyway, right?

> Anything you say can be used against you in court.
>
> -- <cite>Miranda warning.</cite>

During this interview those things will come up. There is a possibility that you are requested to elaborate on 
any given sentence used in your resume. For instance, if you mention __mentoring__ then be prepared to provide
concrete examples about whom you mentored in the past and how.

The following video is pure gold and the YouTuber gets the message accross fantastically. Really a must watch 👇
{% include video id="PJKYqLP6MRE" provider="youtube" %}


## Red flag detector 🚩

I believe that this type of interviews try to spot any big red flags before someone gets hired. It's impossible 
to say if hiring someone will be a success. It's much easier to judge if hiring this person is destined to fail in this company.
That doesn't mean the person is a failure, it means that due to their personality they are not a a good fit for this particular company.
People are different and so do companies. It's all about finding the perfect match.
