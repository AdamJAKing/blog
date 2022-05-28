---
title: "Please Write Automated Tests"
categories:
  - Clean Code
tags:
  - Automated Testing
---

## How Did We Get Here?

Something that I've noticed over my career is how automated tests are often seen as an afterthought. Some 
developers see them as icing on the cake and a nice-to-have, I believe this is incorrect. I truly believe that
any software that is going to be used in a commercial manner should be required to have automated
testing, and to not do so is unprofessional, irresponsible and a slap in the face to your users.

This is a bold statement, some people will say it's a little harsh, but I do believe it to be true and I mean
it with good intentions. In the rest of this post I will explain why I believe in what I have just stated. You 
may disagree with some or all of these points. I can only do my best to convince you. I have worked in the 
industry for almost 10 years now and I like to think that I know the difference between bad code and good code 
and good code always has tests.

## We Don't Have Time To Write Automated Tests

I've heard this statement first-hand on multiple occasions. It is usually muttered during a meeting or a 
period of high pressure due to over-committing and promising things the dev team can't deliver (that's another
blog post!).

Businesses tend to be very short-sighted when it comes to writing code. They don't see the value in adding
tests because the end users don't see or use them. This type of behaviour usually leads to the following

* A new bug is discovered in the system
* The dev team go hunting for the bug
* The dev team find the issue and change some piece of existing code, which fixes the problem
* The change they make breaks something else but the dev team are unaware due to a lack of automated 
testing
* The cycle starts again

The whole process can take hours to resolve. Tests take seconds or minutes to write, and they often stop this
cycle from happening. If you have hours to burn resolving the above cycle then you do have time to write tests.

## Refactoring Without Fear

One of the brilliant aspects of good code is the ability to constantly rewrite parts of code
without being scared of breaking working parts. How many us have written a piece of code and then never
touched it again? How many of us have seen functions that are long and do more than one thing but no one 
dares to touch them? This has become the norm, so much so that developers will often say things such as 
"If it ain't broke, don't fix it". This is wrong. This is how code starts to become legacy

We should constantly be evolving our code and improving it when we see code standards being broken or 
issues such as bugs appear. If code doesn't change then it begins to stagnate. 

In codebase that I am involved with I will regularly advocate for developers to clean-up or rewrite parts that 
they deem unsavoury. I ask developers to do this as they find problems. This means that refactoring code no 
longer becomes part of the backlog and instead becomes part of the normal development lifecycle. It allows 
developers to work together to achieve amazing code quality and take pride in their work.

When we first create automated tests we usually add them to ensure the code is working under conditions
that we expect, as well as various edge cases. They however serve a much bigger purpose long term. They try 
to protect us against breaking working code. If our projects have great test coverage then we can easily rewrite
parts and then check that our existing tests continue to pass. This is truly amazing once you see 
the payoff. That anxious little voice you get in the back of your head when you modify existing code 
essentially disappears. It feels like a superpower.

## Testing External Library Behaviour

One thing I often see is a lack of testing of library code. Developers will pull in a number of libraries
and start coding straight away. This is usually because they think the library they are using won't have
many bugs or that the authors already do automated testing themselves so why bother adding their own?

Now, the question to you. How many times have you had to upgrade a library and been worried about backwards
compatibility issues? Some developers/businesses will actually avoid upgrading libraries due to this fear. This
is completely unacceptable, you're potentially putting your users details at risk. If you're one of the 
developers/businesses that do upgrade, but you don't have automated testing then you likely spend ages looking
around to see if you have broken anything. Automated testing of library code can help with this and allows 
us to achieve two amazing things.

* We can learn how library code works by writing tests against our understanding of the documentation
* The tests we write offer us a form of protection during library updates, as the tests will run against
our previously working understanding of the documentation and code.

I find both of these points fantastic. Whenever we use a library, we have to learn how it works, so
why not just write tests instead of jumping straight into writing production code? Doing so will 
allow us to automatically achieve the second point. 

It can allow us to make sure that our libraries stay up-to-date and that we protect users as much as possible.
This is good code.


## Final Thoughts

I want to point out that even though automated testing is fantastic, it is not a silver bullet. It will
not solve all of your problems and some issues may still slip through the cracks. You will see some developers 
claim that automated tests are pointless because they only test your known working code and edge cases you're 
aware of so some bugs may still remain. I do believe this is shortsighted and just plain wrong. 

I hope I have shown you that automated testing is not just about testing working code and known edge cases but 
that it offers you the freedom to increase your code quality and not be scared of when change happens.