---
layout: post
title: ''
published: true
---

![_config.yml]({{ site.baseurl }}/images/1.png)
## Refactoring to Patterns
### By  Joshua Kerievsky

A Short Review
by Junno Paolo Beringuela
___ 

In the past few months, I had the time to attend knowledge sharing sessions from my team regarding Refactoring and Clean Code. Every friday we did a sharing and talk about what we have read from the two books. We broke it down into chapters and assigned someone to talk about it and share it with the team.
This gave me the interest to further read on this book - Refactoring to Patterns. I find it hard to study design patterns itself and incorprating it into my daily work, and I think this book helps a lot because it gives examples by refactoring an existing code using patterns as solution.

Refactoring to Patterns suggests that using patterns to improve an existing design is better than using patterns early in a new design. We improve designs with patterns by applying sequences of _low-level design transformations_, known as _refactorings_. This gives emphasis on avoiding over-engineering and forces us to write code that are simple and easy to refactor. I liked how the author suggested that using these refactorings, we can limit the change that we make in a legacy code and at the same time not over design a small system.

The author gave a list of refactorings where there is a description of the change, some pros and cons, a before and after code, a mechanics section (which explains the steps of the refactoring in the general case) and an example section. I liked how the author gave real-world examples to help the readers understand it better.

I also saw some similarities from the book Refactoring by Martin Fowler, such as the way the author emphasized the importance of refactoring and also the catalog of refactorings. The author of this book also dedicated a chapter for introducing the different code smells which is important when spotting what areas to refactor in your codebase.

**Design Debt**
Design debt occurs when you don’t consistently
do three things.
1. Remove duplication.
2. Simplify your code.
3. Clarify you code’s intent.

“When do you pay it down?” -> “not fix what ain’t broken" = **Big Ball Of Mud**
If you don’t pay your late fees, you incur higher late fees until it is impossible to repay it.

One of the methods that was most used in this book is the **Compose Method**. It find it VERY relatable in my daily work as I deal with legacy code because often times, I encounter lines of code that I don't even know what it does and how it works. It helps a lot if you cannot understand the logic right away, or if you dont know how you will test a target method or class. Compose Method transforms the logic into small and manageable intention-revealing steps but makes sure that it does not change the behavior of the code.

Another pattern I liked the most was using **Strategy Pattern** to replace the conditional logic. A conditional logic in a certain method can control which specific lines of code to execute per condition.  This switch cases or if's adds complexity to your code. To refactor this, create a strategy class and make the delegation of the logic be the problem of the strategy class. This will make your code cleaner with less duplications.

When you implement the State pattern, you create classes that represent specific states of an object and the transitions between those states. A context delegates state-dependent behavior to a state object. 

So how is it different with the Strategy pattern? The State pattern is often used for a class that must easily transition between instances of a family of state classes, while the Strategy pattern is useful for allowing a class to delegate execution of an algorithm to an instance of a family of Strategy classes as I mentioned above.

Overall, this book is well-structured and is a nice supplement to Martin Fowler's book on Refactoring. Some of the examples can be improved, for example using real-life objects instead of java library classes to explain a pattern for more clarity - but this is just my personal preference. This book is a must-have in our mini-library and I hope we can find a hardcopy for this for reference when we do our refactorings in the team.






