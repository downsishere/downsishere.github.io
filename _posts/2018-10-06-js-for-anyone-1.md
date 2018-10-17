---
layout: post
title: Making Decisions
published: true
subtitle: JavaScript for Anyone Part 1
author: matt
excerpt_separator:  <!--more-->
category: Computer Science
tags:
- js for anyone
- tutorial

---

This is a continuation of the [JavaScript For Anyone](tags.html#js-for-anyone) tutorial. In this post we will discuss how computer programs compare variables, introduce Boolean logic, and talk about how to make decisions.



<!--more-->

# Series Contents

Throughout these tutorials I'd like to cover a few things:

1. [Thinking About Memory](/computer science/2018/10/04/js-for-anyone-0) (variables, assigment, operators)
2. [Making Decisions](/computer science/2018/10/04/js-for-anyone-1) (comparison, booleans, control flow)
3. Repeating (loops, functions)
4. Beginning Node.js (coming soon)
5. Syntax (coming soon)
6. Projects (coming soon)

Access all of the tutorials as they are published [here](/tags.html#js-for-anyone).



# In This Post

- [Comparing variables and values](#comparing)
- [The truth of the Boolean](#booleans)
- [Control flow](#control)
- [Building Blocks](#blocks)

<a name="#comparing"></a>

## Comparing Variables and Values

In the previous post we learned how to conceptualize the creation and editing of variables. So, say we have two variables, `freedom tower floors = 104` and `empire state building floors = 102`. A program can compare two values by using *relational* operators.

| symbol | name                     |
| ------ | ------------------------ |
| >      | greater than             |
| <      | less than                |
| >=     | greater than or equal to |
| <=     | less than or equal to    |
| ==     | equal to                 |
| !=     | not equal to             |

Notice how programming languages use both `=` and `==`, yet the do not mean the same thing. We assign values using `=` while we can check if a variable's value is equal to another value by using `==` (or `!=`).

> It's important to realize that these comparisons work for all types of values such as text, numbers, etc. However, it doesn't make much sense to say a word is greater than or less than another word so just don't use `>`,`<`,`>=`, or `<=` on text.

There isn't really anything we can do with these relational operators until we talk about another key concept of programming: Booleans.

<a name="booleans"></a>

## The truth of the Boolean

There's another type of value that a variable can be assigned- a [boolean](https://en.wikipedia.org/wiki/Boolean_data_type). Booleans may have only two possible values, `true` and `false`. You can probably see uses for this in for programs & algorithims as it allows for the programmer to control **if** an action should occur. In most programming languages, the [relational operators](#comparing) discussed above evaluate to a boolean value. See the examples below, using the sample variables given above the table:

`size = 4`

`squared = 144`

`test = 13`

| expression           | boolean             |
| -------------------- | ------------------- |
| size > 5             | `false`             |
| 56 >= 7              | `true`              |
| (squared / 12) == 12 | `true`              |
| test                 | `true`              |
| 167 < 189            | <input type="text"> |
| 174 != squared       | <input type="text"> |
| squared              | <input type="text"> |
| test = 13            | <input type="text"> |

Most of these examples seem pretty straight forward. But why does just `test` evaluate to `true`? It turns out Booleans are extra handy- then can tell us if a variable exists! This is very useful behavior when working with a large codebase or code that someone might change without you knowing. 

So, now that we have the capability to [compare](#comparison) the values of our [variables](/computer%20science/2018/10/04/js-for-anyone-0.html#variables) with relational operators we need a way to tell our program which way to go.



<a name="control"></a>

##Control Flow 

So let's say that we have an algorithim that tells us to subtract 1 from a value if it the value is greater than 10. Using only the concepts introduced in the previous sections this is impossible- but we are close. To control the way a program evaluates, we'll use the `if` command. Here's an example below:

```javascript
number = 11
if (number > 10) {
    number = number - 1
}
```

So that's a lot of new stuff right there. We already knew how to assign the value `11` to the logical, unique identifier `number`. We also know how to reassign the value to a different value, essentially subtracting `1` from `number`. The `if` command is a bit different, however. Follow the specification below to try and write a similar algorithim to multiply a value by 7 if it is greater than 4:

```python
if (comparison) {
    do something
}
```

<textarea>



