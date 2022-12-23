---
title: Algorithms and Algorithms Analysis
date: August 30, 2022
tags:
  - Articles
  - Code
  - Python
categories: Algorithms

#阅读模式，右下角开启
readmode: true

#封面
cover: /images/Logo/Algorithm_Logo.jpg

#版权
copyright_author: Zehui Liu
copyright_url: https://ahui9605.github.io/

description: ITS495 Special Topics, Algorithms and Algorithms Analysis
---

### What is an Algorithm?

<b>Algorithm:</b> A sequence of definite instructin to perform a certian job

Example1: How to make pancakes?
{% note modern %}

1. In a large bowl, sift together 1.5 cups of flour, 3.5 teaspoons of baking powder, 1/4 teaspoon of salt, and 1 tablespoon of sugar.
2. Pour in 1.25 cups of milk, 1 egg, and 3 tablespoons of melted butter.
3. Mix all the ingredients until smooth.
4. Heat a lightly oiled griddle or frying pan over medium-high heat.
5. Pour appromiately 1/4 cup of the batter, for each pancake, onto the griddle.
6. Cook until brown on both sides.
   {% endnote %}

Example2: How to withdraw money from an ATM?
{% note modern %}

1. Place your bank card into the ATM.
2. Log into the ATM using your personal identification number.
3. Withdraw money.
4. Take your card back.
5. Take your cash.
6. Take your receipt.
   {% endnote %}

<b>Characteristics of Algorithm:</b>

1. Definiteness of each instruction
   {% note modern %}
   We can not have an instruction that says "Add 6 or 7 to".
   {% endnote %}
2. Effectiveness
   {% note modern %}
   It can be done by a person using pencil and paper in a finite amount of time.
   {% endnote %}
3. Termination
   {% note modern %}
   Terminates after a finite number of steps that can be done in a "reasonable" amount of time.
   {% endnote %}
4. Correctness
   {% note modern %}
   The algorithm should do the job it claims to do
   {% endnote %}
5. An algorithm should have <b>zero or more input</b> and <b>one or more outputs</b>.

<b>Analysis of Algorithms</b>

How much time does the algorithm need: <b>Time Complexity</b>
How much space doee the algorithm need: <b>Space Complexity</b>

<b>Data Structure: </b> An organization of a data set
Usually a data structure has several basic operations associated with it, such as search, insert, delete, etc.

<b>Examples of data structures:</b>
{% note modern %}
Arrays, Binary Trees, AVL Trees, Hash tables
{% endnote %}

<b>Time Complexity Examples</b>, the following code fragment is a loop and will repeat 10 times
{% codeblock lang:python %}
for i in range(0, 10, 1):
    print(i)
{% endcodeblock %}

The following fragment is a loop will repeat <b>n</b> times
{% codeblock lang:python %}
for i in range(0, n, 1):
    print(i)
{% endcodeblock %}

{% note modern %}
We say that the time complexity of this code fragment is _O(n)_
{% endnote %}

### Linear Time Complexity

![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/mypic.png "Where, n is the input size and c is a positive constant. ")

| n   | Time, in second, to run the program on computer1 | Time, in second, to run on computer 2 |
| --- | ------------------------------------------------ | ------------------------------------- |
| 1   | 10                                               | 100                                   |
| 2   | 20                                               | 200                                   |
| 4   | 40                                               | 400                                   |
| 16  | 160                                              | 1600                                  |
| 32  | 320                                              | 3200                                  |


### More Time Complexity Examples

{% codeblock lang:python %}
for i in range(0, n, 1):
    print(i)
#Time complexity: O(n)
{% endcodeblock %}

{% codeblock lang:python %}
for i in range(0, n, 1):
    print(i)
    print(2 *i)
#Time complexity: O(n)
{% endcodeblock %}

{% codeblock lang:python %}
for i in range(10, n, 1):
    print(i)
#Time complexity: O(n)
{% endcodeblock %}

{% codeblock lang:python %}
for i in range(0, n, 2):
    print(i)
#Time complexity: O(n)
{% endcodeblock %}


{% codeblock lang:python %}
for i in range(0, n*n, 1):
    print(i)
#Time complexity: O(n^2)
{% endcodeblock %}

{% codeblock lang:python %}
for i in range(0, n, 1):
    for j in range(0, n, 1):
        print("Hi")
#Time complexity: O(n^2)
{% endcodeblock %}

{% codeblock lang:python %}
i = 0
while i < n:
    print("Hi")
    i = i+1
#Time complexity: O(n)
{% endcodeblock %}

{% codeblock lang:python %}
import math
i = 0
while i < math.sqrt(n):
    print("Hi")
    i = i+1
#Time complexity: O(sqrt(n))
{% endcodeblock %}

https://towardsdatascience.com/understanding-time-complexity-with-python-examples-2bda6e8158a7