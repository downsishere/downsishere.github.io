---
layout: post
title: Thinking About Memory
subtitle: JavaScript for Anyone Part 0
author: matt
excerpt_separator:  <!--more-->
category: Computer Science
tags:
- js for anyone
- tutorial

---

Teaching always seems to help me solidify my understanding of any concept. Also, I work and study with Engineers whose programming education consists of reading the Matlab documentation.

> I've chosen JavaScript as the language of choice for this set of tutorials, specifically [Node.js](https://nodejs.org/en/). While [plenty](https://hackernoon.com/the-javascript-phenomenon-is-a-mass-psychosis-57adebb09359) of [valid](https://medium.com/javascript-non-grata/the-top-10-things-wrong-with-javascript-58f440d6b3d8) [criticism](https://medium.com/javascript-non-grata/javascript-is-a-dysfunctional-programming-language-a1f4866e186f) of JavaScript exists, it's not [that](https://hackernoon.com/javascript-a-first-class-language-at-last-209376f69731) bad. After all, JavaScript is the most popular language on [GitHub](https://octoverse.github.com) by a long shot.

This tutorial is written for someone with no programming experience- yet as the target demographic is my college peers, I'm assuming the level of logic and problem-solving skills supposedly present in engineering majors. 

<!--more-->

# Series Contents

Throughout these tutorials I'd like to cover a few things:

1. [Thinking About Memory](/computer science/2018/10/04/js-for-anyone-0) (variables, assigment, operators)
2. [Making Decisions](/computer science/2018/10/17/js-for-anyone-1) (comparison, booleans, control flow)
3. Repeating (loops, functions)
4. Beginning Node.js (coming soon)
5. Syntax (coming soon)
6. Projects (coming soon)

Access all of the tutorials as they are published [here](tags.html#js-for-anyone).

# In This Post

- [Remembering with `variables`](#variables)
- [Math with `operators`](#operators)
- [Working with assignment](#assignment)

# Let's Begin

There will be no code here. Instead, we'll follow a ground-up approach through the building blocks of Computer Science that applies to **most** programming languages you'll ever touch. This isn't a tutorial on Computer Architecture or Web Design or Application Development; instead, it's an introduction to the building blocks of any computer system.



<a name="variables"></a>

## Remembering with `variables`

Think of how you remember things- the **name** of your friend, the **title** of a book you just read, your **make** and **model** of the car you drive. Generally, you wouldn't remember just "John" or "Animal Farm" or "Hyundai" and "Elantra". In your memory there's an identifier attached to each of these values that helps you access them. That's exactly how a computer works, storing **named values** so each item may be "remembered" or changed. This is the lowest level of abstraction you'll probably ever need to know.

In Computer Science, this is colloquially called a `variable`. There's a two important things to know about variables right now: **assignment** and **scope**. Think of assigment as the process of remembering something, creating an identifier and a value. Creating ***meaningful*** identifiers is way more important that one might think. Always create identifiers that logically denote what the matching value actually is. Try and assign some values to custom identifiers following the example below:

| identifier          | value               |
| ------------------- | ------------------- |
| name                | Matt Hall           |
| location            | Columbus, Ohio      |
| age                 | 18                  |
| <input type="text"> | <input type="text"> |
| <input type="text"> | <input type="text"> |
| <input type="text"> | <input type="text"> |

Now think about your brain again. There's certain memories we know no matter what such as your name, age, etc; the simple things that define you. Then think about the more complicated things: your belief system, family history, skills, knowledge, and anything else. Now imagine creating a unique, logical, identifier for every single memory. It sounds impossible, right? That's where scope comes in. Think of scope as a level of access. In programming, just like in your brain, the basic information is defined in the highest, most accessible scope. Lower scopes should contain lesser information only needed by certain parts of the program. There are two scopes: **global** and **local**. Only one global scope may exist, but any number of local scopes can be created. E.g., one local scope could exist for all information on your family members and another local scope might exist for all the things you know about math. For the data below, label each variable **global** or **local**. Be warned, this is highly subjective, but as a rule of thumb if a variable is not crucial (needed by the entire system) it's better to move it to the local scope.

| identifier          | value               | scope               |
| ------------------- | ------------------- | ------------------- |
| name                | John Doe            | global              |
| age                 | 34                  | global              |
| favorite food       | Pizza               | local               |
| <input type="text"> | <input type="text"> | <input type="text"> |
| <input type="text"> | <input type="text"> | <input type="text"> |
| <input type="text"> | <input type="text"> | <input type="text"> |

Observe how as John Doe's name and age are likely crucial bits of information about him, they are given the local scope. In contrast, his favorite food is likely a minor detail that can be put in a local scope.



<a name="operators"></a>

## Math with `operators`

So we've created values and assigned them to unique, relevant identifiers. How do we change them? This is where the brain analogy falls to the wayside, as our brains operate at a higher level than operators do. If you've taken any math class *ever* you've definitely used operators extensively. Many operators exist in mathematics, but the operators needed for basic programs are:

> I'm going to assume you know how to perform the first four operations in the list but the last three are less common outside of programming languages so check out the links if needed. 

| symbol | description                                                  | example |
| ------ | ------------------------------------------------------------ | ------- |
| +      | addition                                                     | a + b   |
| -      | subtraction                                                  | a - b   |
| *      | multiplication                                               | a * b   |
| /      | division                                                     | a / b   |
| %      | [modulus](https://en.wikipedia.org/wiki/Modulo_operation)    | a % b   |
| ++     | [increment](https://en.wikipedia.org/wiki/Increment_and_decrement_operators) | a++     |
| --     | [decrement](https://en.wikipedia.org/wiki/Increment_and_decrement_operators) | b--     |

When working with code, it helps to be able to quickly perform various operations in your head. Do that below:

| expression | result              |
| ---------- | ------------------- |
| 4 + 78     | <input type="text"> |
| 8 % 2      | <input type="text"> |
| 14 / 7     | <input type="text"> |
| 19 % 4     | <input type="text"> |
| 81 * 3     | <input type="text"> |
| 1927 - 58  | <input type="text"> |

So that's neat. But we still don't know how to change the value that we previously assigned to a logical, unique identifier. In fact, we don't even know how to assign a value at all. Luckily, there's a concept called `assignment` that handles that quite well.

<a name="assignment"></a>

## Working with assignment

So we talked for a while about the logical, unique identifiers and values of variables but never explicity created them. By convention, the `=` symbol (equals sign) denotes the assigment of a value to a logical, unique identifier. Everything to the left of `=` is the identifier and everything to the right is the value.

`identifier = value`

`temperature = 84`

`name = Fred`

I know it's very easy, but what is the value of `name` ? of `temperature`? We can call these the **initial values**. Now, let's create a variable with an initial value and then assign a new value to the same logical, unique identifier.

```javascript
city name = Dayton
city name = Columbus
```



After those two assignments, what's the value assigned to `city name`? If you guessed Dayton, you are wrong. A second assignment completely replaces the original assignment. So what if we combine `operators` and `assignment`? While all the examples in the [operators](#operators) section used numbers, all operators work just as well with variables.

> In case you didn't figure it out, operators can't only be used on anything but *numbers* (except when they can, but we'll get to that later)

The assigments below create three variables then change the third's value to the sum of the first two's values.

```javascript
number one = 4
number two = 18
number three = number one + number two
```

That was pretty straightforward. Here's some more complicated practice below- fill out the table to

| code                | value of `final`    |
| ------------------- | ------------------- |
| final = 4           | <input type="text"> |
| number = 123        | <input type="text"> |
| final = 56 + number | <input type="text"> |
| final = final--     | <input type="text"> |
| number = final++    | <input type="text"> |

As you see, we can assign the value from one variable to any other variable. We can also use any operator on a combination of numbers and variables. Remember, operators can only be used on *numbers*.



## Conclusion

That's all for this section. We've learned (at a high level) how computers remember, access, and edit values. We've covered operators and how they can be used to manipulate the (numerical) values of a given variable. The [next post](/computer science/2018/10/17/js-for-anyone-1) will discuss how computer programs compare variables, introduce Boolean logic, and talk about how to make decisions.



[^1]: VAP data is traditionally gathered by the [Institute for Democracy and Electoral Assistance](https://www.idea.int/data-tools/data/voter-turnout/compulsory-voting) for countries around the globe. All VAP percentages cited in the [voting](#voting) section come from [Pew Research](http://www.pewresearch.org/fact-tank/2018/05/21/u-s-voter-turnout-trails-most-developed-countries/).
[^2]: [OCED](http://www.oecd.org), the Organization for Economic Co-operation and Development, is a collective of highly developed, modern nations.

