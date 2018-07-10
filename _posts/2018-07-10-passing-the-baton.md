---
layout: post
title: Passing the baton
date: '2018-07-10T12:00:00-05:00'
tags: []
---
Programming is much more than merely writing code. While it's true that in some jobs (most commonly freelance) a single developer may be responsible for the entire project, more often then not, the developers work as part of a team.

The process reminds me of a relay race. A product owner creates a ticket, which is then assigned to a developer. When the developer completes the code, s/he pushes the code to some kind of a QA environment, where a QA engineer can test the new feature or bugfix. And so on.

In relay races, running is the (relatively) easy part. What often makes or breaks the race is how cleanly you pass the baton!

What does this mean in software development? If you're a developer, here's the advice I have for you:

1. Make sure the code you're writing is clean, readable, and with proper automated tests in place so that the other developers who work on that piece of code in the future (including you) can make further changes easily.

2. If you use version control (and if you don't, you probably should!) make sure to include the ticket number in your commits so that any code changes you introduced can easily be linked back to a ticket. Why certain piece of code does what it does may not be always obvious, and having the ability to refer to the original ticket can be very helpful!

3. After you finish writing the code and deploy it to a QA environment, run a quick manual test to make sure everything is working as expected.

4. Before assigning the ticket to a QA engineer, document the testing steps if needed, so that they can hit the ground running.

The list goes on. You can write documentation, code comments, suggest changes that improve the usability of the product and so on.

As a side note, this advice also applies to other roles. For example, product owners have a really important role in the development cycle because a poorly documented request can lead to unnecessary delays or incomplete or misguided features! Therefore, product managers who write informative and unambiguous tickets are invaluable, but we already knew that. ;)

Lastly, it's worth mentioning that working in this way initially takes more time and effort. But in the long term, the investment is absolutely worth it because not only do you help your team members be more productive, you also improve the quality of the product, which means less consfusion, less bugs and easier code changes down the road.
