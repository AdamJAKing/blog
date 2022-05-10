---
title: "Why I Built This Site"
categories:
  - Clean Code
tags:
  - SOLID
  - DRY
  - KISS
---

One of the things I've noticed during my career is that the quality of code that
some software engineers produce is incredibly poor. It doesn't seem to matter the 
size of the business or how much experience someone has, bad code is everywhere. You
might be wondering what types of things would make code bad. There are so
many things to list but below I have listed a few of the big ones.

* Violating the [SOLID](https://simple.wikipedia.org/wiki/SOLID_(object-oriented_design)?msclkid=4f8f2116d03211ecbd0d449a3fb2cbe6)
principles without justification
* Duplicate code
* Poorly named classes, functions and variables
* Code that requires comment blocks to understand it. Code should be self documenting
and rarely require comments
* Lack of automated testing

From my experience and observations, I believe the reasons for the industry
having so much poor code can be broken down into the following 3 categories.

* Ignorance - Some engineers simply don't know about good coding practices due to a lack
of training or self-study. I personally believe that this category is the real problem.
I've worked with engineers who have 10+ years under their belt but who don't follow good 
standards purely because of ignorance.
* Pressure - Some engineers have become accustomed to working in high pressure 
environments that sacrifice good code over just shipping the product.
* Arrogance - Some engineers simply don't care. It's sad but true, some software engineers
just really don't give a damn about what they ship.

You'll often see engineers trying to justify poor quality with statements such as...

"I was under a lot of pressure to get it done, so I hacked it together"

"It doesn't matter if it's not clean because I understand it"

"Who cares? My code works, doesn't it?"

Though all of these may be true at the time they are often very short-sighted
and will often fail to hold up over a longer period of time.

* Putting code into a system under pressure is likely to cause bugs and there is 
a good chance that there is no automated testing being completed either. Due to this you're
likely going to anger your users and break things in the future if the code needs to change

* It doesn't matter if you understand your code, you need others to understand it.
More importantly, are you going to understand it in 6 months time?

* Your code might work now but is it reusable, maintainable and scalable?

We are professionals, and we are being paid for our services. We should be 
leading the charge when it comes to the development of the software and be proud
of what we can do. I believe that we should be baking good practices into junior developers from 
the moment they are taught their first programming language. That is why I built this site.

How many of us have seen tutorials that name variables "x" or "value"? How many of us
have seen tutorials where there are classes and functions that are dozens of lines long or
do more than one thing? How about hard coding dependencies into files? It's all too common, 
and it doesn't set a good example to new engineers.

So, how can we try and increase code quality in the industry? It's no secret
that learning to code is hard for most people, and we need to be careful to not
add additional stress to new engineers. For this reason I believe the best way
forward is to start small. We need to make sure that when teaching new engineers
that our variables are well named, that our classes and functions don't break the
single responsibility principle from SOLID and the code reads like English. 
I believe that by doing these things that it doesn't add additional hardship of 
learning programming and starts to bake in good practices early on.

As new engineers learn concepts such as classes, inheritance and interfaces
we should slowly introduce additional principles, like all the principles in SOLID 
as well as adding in  [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself?msclkid=f2197fd3d03711ec994e8b8f518b5483) 
and [KISS](https://en.wikipedia.org/wiki/KISS_principle?msclkid=0e5b8aedd03811ec89a7c39be9a6ef49).
We should also ensure that new engineers are taught how to write automated tests. It is far too common
to come across engineers who don't know how to write tests. Tests should not be optional, and we
should expect every engineer to know how to write them. Yes. Even juniors.

I believe that by doing this we can try and ensure that new software engineers start off
on the right footing and try to turn the tide against poor coding standards that currently 
exist in the industry. My goal is help new engineers learn to not just code but to code well.

It's hard to cover everything in such as small amount of time, so 
for further reading I would highly recommend reading Clean Code by Robert C. Martin (Uncle Bob). 
It's a truly fantastic book, and I believe a must-read for all engineers.