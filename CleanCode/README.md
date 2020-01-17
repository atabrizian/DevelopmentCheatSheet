# Clean Code (PHP)

## Introduction

This is a short guide on how to write clean code. This is not a Style guide. Sentences in "" are excerpts From:
Martin, Robert C. "Clean Code: A Handbook of Agile Software Craftsmanship”.

The whole point of this guide can be summarized with:

"The @author field of a Javadoc tells us who we are. We are authors.
And one thing about authors is that they have readers.
Indeed, authors are responsible for communicating well with their readers.
The next time you write a line of code, remember you are an author, writing for readers who will judge your effort.”

## Principles

 - DRY: Don't Repeat Yourself
 - YAGNI: You aren't gonna need it.
 - KISS: Keep It Simple Stupid
 - If it ain’t broke, don’t fix it (probably the attempted improvement is risky and might backfire).
 - Principle of least astonishment
 - High Cohesion and Low Compelling (from GRASP principles)
 - "LeBlanc’s law: Later equals never."
 - There's more than one way to do it!

### SOLID

 - SRP: Single Responsibility Principle
 - Open/Closed Principle: Open for extension, Closed to modification
 - Liskov Substitution Principle: Super classes should be replaceable by subclasses
 - Interface Segregation Principle: No client should be forced to depend on methods it does not use
 - Dependency Inversion Principle: Depend upon abstractions, [not] concretions.

### OOP: Object Oriented Principles:

 - Encapsulation
 - Abstraction
 - Inheritance
 - Polymorphism

## Variables

"You should name a variable using the same care with which you name a first-born child.”
"The name of a variable, function, or class, should answer all the big questions. It should tell you why it exists,
 what it does, and how it is used. If a name requires a comment, then the name does not reveal its intent”

  - Use meaningful and pronounceable variable names
  - Use the same vocabulary for the same type of variable
  - Use searchable names
  - Use explanatory variables
  - Avoid Mental Mapping

    "Readers shouldn’t have to mentally translate your names into other names they already know.”

  - Don't add unneeded context
  - type hint as much as possible

## Comparison

  - Use [identical comparison](http://php.net/manual/en/language.operators.comparison.php)

## Functions

  - Do one thing

    "FUNCTIONS SHOULD DO ONE THING. THEY SHOULD DO IT WELL. THEY SHOULD DO IT ONLY."
"Functions should either do something or answer something, but not both. Either your function should
change the state of an object, or it should return some information about that object."

  - Keep it Small

    "The first rule of functions is that they should be small. The second rule of functions is that they should be smaller than that”

  - Function arguments

    Rule of thumb: a function should have single argument or none. (2 and 3 arguments are also acceptable but not more)

    "There are two very common reasons to pass a single argument into a function.
You may be asking a question about that argument, as in boolean `fileExists("MyFile”)`.
Or you may be operating on that argument, transforming it into something else and returning it”

    "Anything that forces you to check the function signature is equivalent to a double-take.
It’s a cognitive break and should be avoided.”

  - Avoid Side Effects

    "In general output arguments should be avoided. If your function must change the state of something,
have it change the state of its owning object.”
  - Function names should say what they do
  - Don't use flags as function argument

    Using flag as an argument usually means your function is doing more than one thing.

  - Methods should have verb or verb phrase names like
### Indentation

"A source file is a hierarchy rather like an outline."
"Each level of this hierarchy is a scope into which names can be declared and
in which declarations and executable statements are interpreted."
"This implies that the blocks within if statements, else statements, while statements, and so on should be one line
long. Probably that line should be a function call.”

### if statement (Conditional)

   - Avoid negative conditionals
   
### Avoid switch statements

   "It’s hard to make a small switch statement. Even a switch statement with only two cases is larger than I’d like
a single block or function to be. It’s also hard to make a switch statement that does one thing.
By their nature, switch statements always do N things.
Unfortunately we can’t always avoid switch statements, but we can make sure that each switch statement is
buried in a low-level class and is never repeated. We do this, of course, with polymorphism.”

### Avoid type-checking

   Instead of deciding to do different things based on "instanceof", try using polymorphism.

### Remove dead code

   YAGNI! (Even if you happen to need it, source code control systems keep track of these codes for you.)

## Comments

### Don’t comment bad code — rewrite it.

   "when you find yourself in a position where you need to write a comment, think it through and see whether
there isn’t some way to turn the tables and express yourself in code. Every time you express yourself in code,
you should pat yourself on the back. Every time you write a comment, you should grimace and feel the failure of
your ability of expression."

### Avoid noise comment

   "Sometimes you see comments that are nothing but noise. They restate the obvious and provide no new information.”

### Comments can lie

   The only truth can be found in code.

## Code Smells

### Comments:

 - Inappropriate Information
 - Obsolete Comment
 - Redundant Comment
 - Poorly written comment
 - Commented-out code

## Design Patterns
   Although design patterns are just reusable forms of a solution to a design problem and not
   clean coding rules, knowing them will help you in organizing your code in a way that 
   most probably you'll end up with a clean code.

 - [https://designpatternsphp.readthedocs.io/en/latest/](https://designpatternsphp.readthedocs.io/en/latest/) website is descriptive and compact enough.
