---
layout: essay
type: essay
title: "Good Answers Are Cheap. Good Questions Are Not."
image: ../img/smart-questions/rtfm.png
date: 2026-09-10
published: true
labels:
  - Software Engineering
  - StackOverflow
  - Communication
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## Everyone can get answers now

Almost any factual question can be answered in seconds now. If I want to know what a rest parameter does or why my for loop is off by one, I can ask an AI model or just Google it and be done. Because of that, there are very few questions left that you truly cannot answer on your own. So when everyone is able to get quick answers, the real difference between people becomes the kind of questions they ask. If we can all get answers, the question is whether you are asking good ones.

Eric Raymond's essay [How To Ask Questions The Smart Way](http://www.catb.org/esr/faqs/smart-questions.html) was written way before AI assistants existed, but the core idea still holds up: the people (and now the machines) most able to help you will help you best when you do your homework first, give context, get specific, and make the question easy to act on. In this essay I look at one real StackOverflow question that gets this right, one made up question that gets it wrong, and what I learned about asking questions this semester.

## A smart question: two million people had the same one

The question [Why is processing a sorted array faster than processing an unsorted array?](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array) was asked by user GManNickG in June 2012. It is the most upvoted question in StackOverflow history, with over 27,000 upvotes and close to two million views.

The asker noticed something weird: a loop over an array ran about six times faster when the array was sorted first, even though sorting should not change the amount of work being done. Instead of posting "my code is slow, why?", he posted a short, complete, runnable C++ program, the actual timing numbers he measured (11.54 seconds unsorted versus 1.93 seconds sorted), and proof that he had already dug into it himself: he ported the same test to Java and got the same behavior, which ruled out a compiler quirk. The title states the exact thing he observed. There is nothing vague to interpret and nothing missing if you want to reproduce it.

That is basically Raymond's checklist in one post: a precise subject line, a minimal reproducible example, evidence of prior effort, and a question with one concrete, answerable core. The response shows what that buys you. User Mysticial wrote an answer, now sitting at over 35,000 upvotes, explaining CPU branch prediction with a now famous analogy about a railroad junction operator guessing which way to flip the switch. The page became a canonical reference that the community still points people to today. One well built question turned into a resource that taught low level CPU behavior to two million readers. That is what a good question can buy.

## A not so smart question

For contrast, here is a question written the not smart way. As the assignment suggests, this example was AI generated instead of pulled from StackOverflow, since the community there closes or deletes questions like this pretty fast:

> **Title: URGENT!!! my code doesnt work please help ASAP**
>
> I am building a website and the javascript is broken. Nothing happens when I click the button. I tried everything and nothing works. This is due tomorrow. Can someone fix this for me??? I can send the files to whoever wants to help.

And the kind of responses it earns:

> "What does 'doesn't work' mean? What button? Post your code." (then no reply for six hours)
>
> "Nobody is going to download your files. Read how to create a minimal reproducible example and edit your question." (question sitting at minus two)
>
> Closed: *Needs details or clarity.*

The responders are not even being mean here. They are asking for the things the question should have included in the first place. The asker pays for the missing context with a full round trip of waiting, and probably never gets an answer at all. Every precept the sorted array question followed is violated: no specific title, no code, no error message, no sign of effort, and the "URGENT" pressure that Raymond specifically warns against, because your deadline is not a volunteer's problem.

## Knowing who to ask is part of the skill

Something this exercise made me realize is that a smart question is not just about phrasing. It is also about sending it to the right answerer. This semester I hit an inconsistency between a chart and a table in one of our practice WODs. I asked an AI assistant about it first and it struggled, because the important information was inside an image of a chart and the model could not really work with it. My professor answered the same question immediately, because he had context the AI did not have.

That gave me a rule I use now: ask AI the questions that documentation can answer, and ask humans the questions where the information is stored in somebody's brain. You would not ask an AI what your professor's late policy is. Unless it is written in the syllabus, that knowledge only exists in one place, and the only way to get it is to ask the person, and to ask well. The smartest question in the world sent to the wrong answerer is still a wasted question.

I also see this from the other side when I tutor beginning programmers. The questions that are easy to help with are specific and have a concrete outcome attached, like "will approach A or approach B work better for doing X?" The impossible ones are vague, like "what is the purpose of all of this?" There are so many ways to give something meaning that a vague question forces the helper to answer twenty possible questions and hope one of them was yours.

## Smart questions in the AI era

I do not think AI makes this skill obsolete. My experience says the opposite: prompting well IS asking smart questions, just at higher speed and volume. When I prompt, I try to be straightforward, precise, and not repetitive, and I state boundaries explicitly, meaning what I want, what I do not want, and what form the answer should take. More than anything, my smart questions come down to one thing: have I given all the right context? Once the context is right, every question I ask lives inside that context, and the answers get dramatically better. That is Raymond's advice applied to a machine.

So the takeaway for me is not "be polite on StackOverflow." It is that asking questions is a real engineering skill with a real payoff. The sorted array question turned one developer's curiosity into a resource for two million people. The lazy question earned a lock and silence. Getting answers has never been easier, which is exactly why the questions are the part worth practicing.

---

*AI disclosure: I used Claude (Anthropic) to support this essay. I dictated my answers to a set of interview questions about my experiences and opinions, and the AI transcribed and organized my points into essay structure and cleaned up grammar. The "not so smart" question example was AI generated, as the assignment suggests. The experiences, opinions, and conclusions are my own.*
