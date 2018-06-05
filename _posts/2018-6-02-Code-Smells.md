---
layout: post
title: ''
published: true
---
![_config.yml]({{ site.baseurl }}/images/smell.png)

## Code Smells and How To Refactor Them

by Junno Paolo Beringuela
___

In my last post, I started reading _Clean Code : A Handbook Of Agile Software Craftsmanship by Robert C. Martin_. As I read thru the first phase of the book, I understood how the author emphasized the need to write clean and simple code. He has also shown the readers how an unstructured code looks like and why it is bad. As the title says, this post will be focusing on these 'unstructured code', and the anti-patterns of clean code - also known as Code Smells.

Code smells happen for a lot reasons, can be because of inexperience, laziness, lack of abstraction, or simply just overthinking a simple problem. A lot of programmers, including me, are guilty of this. This concept is a perfect example for the metaphor - _"when there is smoke, there is fire"_. It signals out to the members of the team that code smells are a risk, and can be a sign of a hidden design flaw.

The author gave out a lot of code smells, and emphasized that that specific chapter is a collection of code smells that they encountered in their years of experience and that it may not contain all possible issues in a codebase. I loved how he categorized these into their use cases and he also suggested ways to solve it. He also recommended some references and books from his friends which can help. I chose to use_ Refactoring - Improving the Design of Existing Code by Martin Fowler_ as it also gives out a list of handy techniques for refactoring code smells.

Here are some of the common code smells that somehow I think is highly notable and highly relatable :

1. **Code Duplication** - As the name says, there are duplicated code in your project. Can be a sign of inefficiency and a lack of abstraction on the design. It is easy to spot these using your favorite IDEs, but the most importanting when adding feature is that you check if an implementation is already existing and how you can leverage those and taking out those that are similar to different classes, this is called Extract Method.

2. **Feature Envy** - When you start to make functionalities in your class that mostly requires help from another class, then your code might be guilty of this code smell. Use move method to transfer those functionalities in its respective class.

3. **On If/Else or Switch/Case statements** - If you are using switch case which appears to be the same condition in similar parts of your code, then you might want to consider making use of polymorphism instead. First is using Extract Method to setup the conditional statement elsewhere, and then using some design patterns such as Factory pattern then use Replace Conditional with Polymorphism.

4. **Bloated Constructors** - The manier the parameters are in your functions, the higher the complexity of your functions is. It only means that the function does not do one thing and one job at all. The book prefers having 2 or 3 at most for your function parameters. 

5. **Misleading Information** - Adding authors, explaining the change and writing down story numbers or feature numbers can only add to the eyesore that the comments add to your function. Avoid using those and rely on your source control history for documentation and for tracking.

6. **Commented-Out Code** - Maybe some of your team members want to keep old code as references to why the change was made, or just to keep it because they think they will need it for future implementation again. Please explain to them the use of version control systems instead.

7. **Inconsistency **- This happens when there is lack of standardization or lack of implementation of it in your team. For big projects like ours, there may be a lot of programmers who handle your project which came from different background and coding styles. Try your best to impose a standardization for uniformity.

8. **Naming variables** - This can be one of the hardest things to decide on when writing code. Make sure to make your names as descriptive as possible. After all, we want to avoid using comments so make your names serve as documentation to your readers and to yourself as well.

9. **Insufficient Tests** - Focus on breaking your code. On writing tests, it is best to have a QAs mindset and try to think about all the ways your code can go and write a test for it. TDD can be a lot of help on this because it makes sure that you have a test as you write your production code. An anti-pattern for these is writing to many tests that are actually redundant and can lead to waste.

10. **Tests Should Be Fast** - Firstly, we want to enable fast feedback. Having tests that run fast can signify a lot of good points in your code. For one, you have a nicely decoupled function. Another is that you wrote a test just to check a simple thing that you wrote for a production. In TDD, fast tests meaning faster development.
___

These are only some of the many many code smells that were mentioned in the books above and I leave it to you guys to learn from it and find out the rest. The authors suggested to make use of those chapters as guides/references where we can always go back and check if we encounter something similar to that and we want to find out the appropriate solutions. We can also find code smells that we think is not included in the list, but for now I think having these standard solutions to our common problems are of great help to our messy codes.
