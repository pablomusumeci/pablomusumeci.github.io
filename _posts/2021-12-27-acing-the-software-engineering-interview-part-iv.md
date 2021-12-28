---
title: Acing the Software Engineer Interview - Part IV
excerpt: System design, behavioral interviews and negotiating offers
last_modified_at: 2022-01-07
categories:
  - Interviewing
tags:
  - Interviewing
toc: true
toc_label: The Last Dance
toc_icon: code
toc_sticky: true
---

This is the fourth in a [series of blog posts](https://pablomusumeci.com/categories/#interviewing) 
where I describe my interviewing experience and thoughts in detail.

Once you've passed the coding interviews, there are still two more interviews to come.
I think that the coding interview is the hardest and the one that requires the most preparation but
you needed to be successful at all of them if you want to get your dream job.

# System design interview

This interview is mostly about designing high-level components (boxes and arrows) for solving a very general scenario.
The problem will be described with very few details and is up to you to go and capture all the requirements.

Requirements are divided into two:
- **Functional requirements**: What should the system do?
- **Non-functional requirements**: Attributes of the system such as scalability, availability, fault-tolerance, latency, data integrity, security, etc.

The number of things that can be discussed is pretty much endless, so your interviewer will guide you through the
areas they consider most important to be discussed. 

System design interviews can touch a bit of every topic but dive deep in only a handful.
Some people do more emphasis on the type of database used while others care more about designing a clean API.

## Distributed systems

> A distributed system is one in which the failure of a computer you didn’t even know existed can render your own computer unusable.
>
> -- <cite>Leslie Lamport</cite>

Here you have a shortlist of (very complex) topics you should read about:

- Understanding the [CAP theorem](https://en.wikipedia.org/wiki/CAP_theorem) and its importance
- Consistent hashing and its applications
- Consistency levels and their trade-offs
- Types of databases and when to use which
- Sharding and replication
- Load balancing and API gateways
- Publish-subscribe pattern
- [API versioning](https://stripe.com/blog/api-versioning)
- [Websockets and RPC](https://eng.uber.com/real-time-push-platform/)
- Consensus protocols (no need to go too deep here)

{% include video id="aXD4tWbkoJo" provider="youtube" %}

There is no good or bad solution, it all depends on the problem you are trying to solve and the trade-offs you are
willing to make. You might prefer availability over consistency when calculating the number of likes on a social
media post. There it's not a big deal if you show incorrect (as in stale) data for a while as long as you show *something*.

Whereas in systems that handle money we are usually more worried about strong consistency (calculating the right value)
at the expense of some downtime.

## Avoid naming names

I highly encourage you to avoid naming specific technologies and just stay with the most generic abstraction possible.
Instead of saying "I would cache things in Redis", just say that you would use an in-memory datastore. 
Use a NoSQL database in place of "I would use MongoDB". 

The moment you put a name out there your interviewers are going to start asking questions about that specific technology
and why you've made that specific choice.
Restrain yourself from mentioning technologies you are not too familiar with. For this kind of situation, I always say 
something like:

> Disclaimer, I've never worked with this technology but I read that **${BUZZWORD}** is generally used to solve this kind of problem.
>
> -- <cite>Pablo</cite>

You should at least know the very basics of **${BUZZWORD}** technology and why people recommend it for solving this problem?
Don't just talk for the sake of talking. In general, we prefer to work with someone who admits when they don't know something
instead of bullshiting their way out of a situation.

Not knowing is fine, dishonesty is not. This interview can bring up a wide variety of topics and no one is expected to
be an expert in all of those. It's more about how would you tackle the *unknowns* and your thought process for that.
Identify single points of failure and bottlenecks. Be mindful of trade-offs and explicitly mention them to your interviewer.


## Practice is the best teacher

My way of learning about these topics is to first start by reviewing existing architectures and then go deep into theory as needed.
For instance, if you first understand the problem consistent-hashing is trying to solve, then the specifics will make much more sense to you.
Don't read theory for the sake of reading theory. It won't hurt you but it will also not be the best usage of your time. You need tools
to solve problems. 

Which kind of problems? Here you have a not so short list I recommend for practicing:

- Design a rate limiter
- Design a URL shortener (like TinyUrl or Pastebin)
- Design a distributed ID generator (like [Twitter Snowflake](https://blog.twitter.com/engineering/en_us/a/2010/announcing-snowflake))
- Design a web crawler
- Design a notification system
- Design a ticketing system (like Ticketmaster or BookMyShow)
- Design a hotel booking system (like Booking or Airbnb)
- Design a news feed system in a social media platform
- Design a chat system

## Resources 
- [System Design Interview – An insider's guide](https://www.amazon.com/System-Design-Interview-insiders-Second/dp/B08CMF2CQF) is a fantastic source of 
examples for preparing the SD interview. If you don't know how to start, please start with this book.

{:refdef: style="text-align: center;"}
![system design book](/assets/images/acing-the-software-engineering-interview/system-design-book.jpg)
{: refdef}

- An interviewer from *FAANG* recommended me the following course [Grokking the system design interview](https://www.educative.io/courses/grokking-the-system-design-interview). I haven't used it but I heard amazing things about it.

I also wanted to share a few YouTube channels that I used:
   - [Hussein Nasser](https://www.youtube.com/user/GISIGeometry)
   - [Gaurav Sen](https://www.youtube.com/channel/UCRPMAqdtSgd0Ipeef7iFsKw)
   - [Code Karle](https://www.youtube.com/c/codeKarle)
   - [Tech Dummies Narendra L](https://www.youtube.com/channel/UCn1XnDWhsLS5URXTi5wtFTA)
   - [SystemDesignInterview](https://www.youtube.com/c/SystemDesignInterview/)


Those channels are more about practical examples and interview preparation but if you want more something theoretical check [Martin Kleppman's channel](https://www.youtube.com/channel/UClB4KPy5LkJj1t3SgYVtMOQ). He is the author of the famous *Designing Data-Intensive Applications: The Big Ideas Behind Reliable, Scalable, and Maintainable Systems*.

{:refdef: style="text-align: center;"}
![Martin Kleppmann](/assets/images/acing-the-software-engineering-interview/martin-kleppmann.png)
{: refdef}

Also some blogposts I liked:
- [How Discord Stores Billions of Messages](https://blog.discord.com/how-discord-stores-billions-of-messages-7fa6ec7ee4c7)
- [Sharding & IDs at Instagram](https://instagram-engineering.com/sharding-ids-at-instagram-1cf5a71e5a5c)

# Behavioral interviews

I always disregarded the soft-skills interview as I consider myself a very talkative and easy-going person. The stereotypical programmer
is introverted, socially awkward, and intellectual. I recognize parts of me that match the standard nerd although
I always considered myself *normal* enough to pass what I considered to be *the psychopath test*.

{:refdef: style="text-align: center;"}
![standard nerds](/assets/images/acing-the-software-engineering-interview/standard-nerds.gif)
{: refdef}

At big companies though, this interview is much more than just a check to ensure that you are not a wacko.
Behavioral interviews are there to check if you are a match for the company's culture.
A company's culture is not constituted by its free lunch, Friday drinks, and game rooms. 
The culture of a company is its DNA.


## Compatibility check

I'm not going to go too deep into what embodies a company's culture but I will summarize it in a quote extracted from this [blog post](https://camillaboyer.medium.com/why-cultures-fail-3151e72d3ca8).

> Culture is how we do things here and how people act when nobody is watching.

Interviewers will throw at you **open-ended questions** about your past experiences to understand who you are. 
Why not ask that directly? Because stories are a medium that most truthfully reflect our core values compared to just describing our strengths and weaknesses.
Stories teach. Let the story speak to the interviewer in its own way and skip the need to tell them what to think.
An example of a situation where you exhibited a particular trait is much more convincing than an empty statement about your persona.

All these questions start with something similar to  "Tell me about a time where..."

- You received tough feedback
- You had to provide tough feedback
- You built out a process
- You made a mistake
- You proposed an idea and was not agreed on
- You convinced someone to change their mind
- You mentored someone
- A project you were working on failed
- You didn't have enough resources but still had to deliver a project

How should we approach those types of questions?

## The hero's journey

This interview is all about telling a good story. We are fascinated by stories.
That's the reason why we love watching movies and reading books.
It's critical that you pick good stories to illustrate your past experiences.

A good story does not have to depict you as a perfect person or employee. Think about it, would you like
to see a movie where the main character is flawless? That would be pretty boring.

The heroes we love are fragile and flawed. They make mistakes and don't always win. What we love about them is 
that each failure allows them to emerge stronger than before.

> We do not learn from experience, we learn from reflecting on experience.
>
> -- <cite>John Dewey</cite>

It's natural to try hiding your weaknesses during interviews but you shouldn't. Self-reflection
shows a person that wants to improve. You know you are not perfect, you know there are areas you should improve but you are a work in progress.

You should carefully prepare and pick the stories you are going to be using during the interview. Think hard about all
your previous experiences because picking the right story to tell is not an easy task. You want to select a story
that makes you look good but not perfect.


{:refdef: style="text-align: center;"}
![heroes journey](/assets/images/acing-the-software-engineering-interview/heroes-journey.png)
{: refdef}

Think about stories where you...

- Demonstrated initiative instead of just complaining.
- Took risks but without being reckless.
- Made a mistake while trying to do something with good intentions.
- Led by example and inspired others.
- Decided something that seemed right at the moment but ended up being the wrong call.

You might come up with a few potential stories that can answer each question. Select the ones that 
best showcase the reasons why you should be hired.

:warning: Preparing the stories is not considered *cheating* the interview. You will be advised before this interview
to prepare these examples. It's very challenging to come up with good examples on the spot. Use this opportunity to
reflect on your career and what you've learned in each one of your jobs. 

## A good story needs only a good storyteller

Now that you have a few candidate stories, it's time to write a script. You want to narrate the situation providing
enough context but without going too deep into unnecessary details. 

Some people suggest using the [STAR](https://www.themuse.com/advice/star-interview-method) method.

- **S**ituation
- **T**ask
- **A**ction
- **R**esult

I rather use an old-time classic like the [three act structure](https://en.wikipedia.org/wiki/Three-act_structure).
Such construction is used in every single good story ever told. Setup, confrontation, and resolution.

Now is where the fun beings. Use a friend to practice your story-telling. Just explain the situation in around five minutes.
Request them to ask questions if something is not clear. You need to get rid of the plot holes.
Telling the same story over and over helps you master how that particular story should be told. 

Think about the best stories you share with your friends or that story your grandpa always brings up at family reunions.
Keeping a good pace is key. You want to speak slow enough so that the story is easily absorbed but not so slowly that the listener's mind checks out of the room.


## What is the cost of lies?

> Every lie we tell incurs a debt to the truth. Sooner or later, that debt is paid.
>
> -- <cite>Chernobyl, HBO</cite>

You might think that you don't have any good stories to tell, that nothing truly remarkable happened to you at work.
Perhaps you are considering inventing a story that shows you have all the ingredients the interviewer is looking after in a candidate.

I'm going to tell you why that's a terrible idea. By doing this you are showing your interviewers a big fat red flag.
Interviewers are pros. They had this interview hundreds of times before. They know how a good answer looks like and they can smell
a false story from miles away.

There will be two or three nested questions about your stories. It will be impossible for you to maintain a credible lie.
They will catch you red-handed and that's the worst possible outcome of the interview. Dishonesty means 
instant disqualification.

{:refdef: style="text-align: center;"}
![disqualified](/assets/images/acing-the-software-engineering-interview/disqualified.gif)
{: refdef}

Lying doesn't benefit you or the company. You can only thrive in a workplace where you are a happy camper.
If you are not a mutual match then trying to force the relationship through lies will manifest later on and will be painful for all parties involved.


## The Miranda warning

If you are at this interviewing stage, you probably wrote your resume a few months ago and completely forgot about everything that's mentioned in there.
You might even have bent the truth a little bit to make your resume more attractive to recruiters. No one pays full attention to everything
that's written there anyway, right?

> Anything you say can be used against you in court.
>
> -- <cite>Miranda warning.</cite>

During this interview, those things will come up. There is a possibility that you are requested to elaborate on 
any given sentence used in any part of your resume. For instance, if you mention __mentoring__ other engineers four years ago, then be prepared to provide
concrete examples about whom you mentored in the past and what was the outcome.

The following video is pure gold and the YouTuber gets the message across fantastically. A must watch 👇
{% include video id="PJKYqLP6MRE" provider="youtube" %}


## Red flag detector 🚩

I believe that this type of interview tries to spot any big red flags before someone gets hired. It's impossible 
to say if hiring someone will be a success. It's much easier to judge if hiring this person is destined to fail at this particular company.
That doesn't mean the person is a failure, it just means that due to their personality they are not a good fit for this one company.
People are different and so do companies. It's all about finding the perfect match.

# Getting an offer you can't refuse

> Great news! - I received positive feedback from the team about your most recent interviews, and we'd like to make you an offer! 

{:refdef: style="text-align: center;"}
![congratulations](/assets/images/acing-the-software-engineering-interview/congratulations.gif)
{: refdef}

That's it, you've made it. The long journey has come to an end. Yes but no. This is not over until the contract is signed (at least digitally).
Now we have to play a different kind of game.

You might think that negotiating is not your thing. You rather take whatever the company offers to avoid having that uncomfortable conversation about money.
You don't want to look like a greedy person, you just want a better job that pays more than the one you currently have. How much more? Whatever the company offers you is fine...

> You do not get what you want. You get what you negotiate.
>
> -- <cite>Harvey Mackay.</cite>

What's the point of risking a job offer you were planning to accept for an extra 5%? **WRONG**. You are most certainly not putting your offer on the line
and the amount you are leaving on the table it's for sure much larger than just 5%.

Negotiating a good offer can be an instant **20%** (or more) raise and only takes you a few short meetings and some nerves of steel.
I'm not going to lie, is not going to be easy. Well, the situation is indeed not hard at all but your mind will freak out about it. 
The fear of losing everything will [cloud your judgment](https://en.wikipedia.org/wiki/Framing_effect_(psychology)). We are risk-averse creatures.

{% include video id="u9BoG1n1948" provider="youtube" %}

## What gives you leverage?

If you want to negotiate a better offer you need to be honest with yourself about who has the better hand. The company
already invested lots of their time and resources interviewing you. And they want you, that's why they extended this offer to you.
Only a small percentage of applicants make it to the end of their lengthy and complex interviewing pipeline. If you decline their offer is a big hit for them, they
will not let you walk away from them that easily.

There are only two things that give you leverage for negotiating a better offer.

- **Acing the interviews**: They love you. You impressed everybody with both your technical and soft skills. All the interviewers said **strong hire**
and they are willing to do whatever it takes (within the limits of what's ~~reasonable~~ possible) to get you on board. 
- **Having competing offers**: They need to offer you more because they are afraid of losing you to another company that is willing to put more money on the table. You should mention that money is not the only 
thing you care about, but you also don't want to feel you are missing something. They will do their best to match your best offer to make sure that money is not
the deciding factor in the negotiation. 

If you can combine both of these situations then you have the recipe for negotiating a very nice compensation package. Congratulations again 🎉!

## NANANANA BATNA
When you have multiple offers from good companies, you have a very strong **BATNA** and that puts you in the perfect position. 
What does *BATNA* mean? It stands for **Best Alternative To a Negotiated Agreement**. 

It's the alternatives you or the company has in case the deal doesn't work. 
Each party involved in the negotiation has its own *BATNA*.

{:refdef: style="text-align: center;"}
![congratulations](/assets/images/acing-the-software-engineering-interview/batman.gif)
{: refdef}

Let's look at this particular case in more detail. The company's *BATNA* is to keep interviewing more people to fill the spot.
If they have one position and ten prospects to fill it, then I'm sorry but you are not *that* special for them. But in the software business, the opposite is more likely to be the case, especially for more senior positions.

If the company struggles to find strong candidates that meet their bar, then their *BATNA* (the deal is over because you rejected them) kind of sucks. 
Whereas your *BATNA* is just going with one of the other amazing companies that extended you an offer. The more alternatives you have the stronger your *BATNA* becomes.
The more desperate you are, the weaker your *BATNA* becomes.

I have to admit it, I love how the word *BATNA* sounds.

## Resources

There are some amazing resources written about this subject. Please go ahead and prepare yourself for the negotiation phase in the same way you've prepared for all the other types of interviews.

These three links are undoubtedly a **must-read**. They are also written in a very entertaining way so it will be both fun and educational.
- [Ten Rules for Negotiating a Job Offer](https://haseebq.com/my-ten-rules-for-negotiating-a-job-offer/)
- [How Not to Bomb Your Offer Negotiation](https://haseebq.com/how-not-to-bomb-your-offer-negotiation/)
- [Salary negotiation](https://www.kalzumeus.com/2012/01/23/salary-negotiation/)

Optionally, if you are fascinated by this topic as I am, you should read 
[Never Split the Difference](https://www.amazon.com/Never-Split-Difference-Negotiating-Depended-ebook/dp/B014DUR7L2) by
former FBI hostage negotiator Chris Voss.

{:refdef: style="text-align: center;"}
![Never split the difference](/assets/images/acing-the-software-engineering-interview/never-split-the-difference.jpeg)
{: refdef}

I guess that's pretty much it. I hope my experiences helped you in some way. I counted with the support of all 
my friends and family while going through this very stressful process. Although I can't really complain, I'm very
satisfied with everything I've learned along the way and the job I landed.

Thanks for reading and if you have any questions don't hesitate to drop me a message on any of my social media accounts,
I will be more than happy to help anybody in advancing their careers.