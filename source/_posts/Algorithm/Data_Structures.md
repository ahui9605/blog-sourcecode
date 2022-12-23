---
title: Data Structures
date: October 11, 2022
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

description: ITS495 Special Topics Algorithms
---

### Data Structure

Definition: A data structure is a set of objects, relationships between objects, and a set of operations that can be applied to the set.
Examples of objects:
{% note modern %}
numbers(int, double,…), strings, instances of classes(Cars, Customers,…), etc.
{% endnote %}
Examples of relationships:
{% note modern %}
next, previous, left, right, up, down, etc.
{% endnote %}
Examples of operations:
{% note modern %}
insert, search, delete, etc.
{% endnote %}
Examples of data structures:
{% note modern %}
arrays, stacks, queues, heaps, trees, hash tables, …
{% endnote %}

### Arrays and Lists

Array is a very basic data structure consisting of a set of similar objects, accessed by index.

Advantages of arrays:

- effectively stored inside the computer, no overhead per object(no space is wasted).
- fast access(by the index) to all of its objects at O(1) time.

Disadvantages of arrays:

- not completely dynamic (fixed size arrays)
- Insertion and deletion of an element in the array requires to shift O(n) elements on
- average, where n is size of the array.

#### Arrays in Python


{% tabs test4 %}
<!-- tab Program -->
{% codeblock lang:python %}
import numpy as np
myArray = np.zeros(4, dtype='int32')
#creates an array of type int32, size 4, and initialize it to 0
myArray[0] = 6
myArray[1] = 7
myArray[2] = 8
myArray[3] = 9
print("myArray size is: ", myArray.size )
for i in range(0, myArray.size, 1):
    print(myArray[i])
{% endcodeblock %}
<!-- endtab -->

<!-- tab Output -->
{% note modern %}
myArray size is: 4
6
7
8
9
{% endnote %}
<!-- endtab -->
{% endtabs %}

#### Lists in Python

In Python,  lists are very similar to arrays but they are implemented differently. 

Lists are dynamic, the size is not fixed and they can have more than one data type in the same list. Lists require overhead (in space and time).


{% tabs test4 %}
<!-- tab Program -->
{% codeblock lang:python %}
List1 = [2, 4, 6, 8, 10]

for i in range (0, len(List1)):
    print(List1[i])

List1.append(20)
List1.insert(2, 40)
List1.remove(6)
print(List1)
{% endcodeblock %}
<!-- endtab -->

<!-- tab Output -->
{% note modern %}
2
4
6
8
10
[2, 4, 40, 8, 10, 20]
{% endnote %}
<!-- endtab -->
{% endtabs %}

#### Two-Dimensional Arrays in Python
In an n-dimensional array, the index of each element is an n-tuple of positive integer numbers. 

The most commonly used multidimensional array is the two-dimensional array where the index of each element is an ordered pain of positive integers. 

Two-dimensional arrays are also knowns as  tables or matrices. 

{% tabs test4 %}
<!-- tab Program -->
{% codeblock lang:python %}
import numpy as np

matrix = np.zeros((2, 3), dtype='int32')
#creates a matrix  of dimension 2, type int, and
#initialize it to 0's
matrix[0][0] = 3
matrix[0][1] = 4
matrix[0][2] = 5
matrix[1][0] = 6
matrix[1][1] = 7
matrix[1][2] = 8
for i in range(2):
    for j in range(3):
        print(matrix[i][j], end =" ")
    print(" ")
print("matrix dimension is: ", matrix.ndim)
{% endcodeblock %}
<!-- endtab -->

<!-- tab Output -->
{% note modern %}
3 4 5 
6 7 8 
matrix dimension is:  2
{% endnote %}
<!-- endtab -->
{% endtabs %}


### Queues

A queue is a data structure that supports the operations:

1. enqueue(x)// insert x into stack
2. dequeue(x) // delete x from stack

![](/images/Algorithm/Queues1.png "")


{% note modern %}
A Queue helps to manage the data in the  First In First Out (FIFO) method.
In Queue, random access is not possible
{% endnote %}

A queue can be implemented  as a simple array or as a class.
To implement the operations of a queue, one can maintain two global indices: head, and tail.  

The basic operations can be coded as follows:

{% tabs test4 %}
<!-- tab Enqueue -->
{% codeblock %}
Procedure enqueue(Q, a)
begin
   tail = tail +1; 
   Q[tail] = a;
end
{% endcodeblock %}

<!-- endtab -->

<!-- tab Dequeue -->
{% codeblock%}
Procedure dequeue(Q)
begin
  head = head + 1; 
end
{% endcodeblock %}
<!-- endtab -->
{% endtabs %}

#### Priority Queues

![](/images/Algorithm/Queues2.png "")

<b>Example:</b> Suppose we have the following 6 jobs with their priorities:

{% note modern %}
A-2, B-3, C-2, D-1, E-2, F-2 
{% endnote %}


Suppose these jobs are scheduled using a regular queue by performing the following operations:

{% note modern %}
enqueue(A), enqueue(B), enqueue(E), enqueue(C), enqueue(D), enqueue(F) 
{% endnote %}

Now suppose the jobs are processes by calling the dequeue operation.

These jobs will be processes look like this: 
{% note modern %}
F - D - C - E - B - A
{% endnote %}



### Singly Linked Lists

A <b>linked list</b> is a linear data structure, in which the elements are not stored at contiguous memory locations. 

Every node of a singly-linked list contains  a value and a link to the next element.

![](/images/Algorithm/Linked_Lists.png "")

<b>Example</b>: Supposed we want to store the following numbers in a singly-linked list:

{% note modern %}
6, 8, 9, 12, 56, 78
{% endnote %}

Then we can store the information as (value, link) as follows:

{% codeblock lang:python %}
#assuming that 0 represents a null link
V[1] = 6, L[1] = 2
V[2] = 8, L[2] = 3
V[3] = 9, L[3] = 4
V[4] = 12, L[4] = 5
V[5] = 56, L[5] = 6
V[6] = 78, L[6] = 0 
{% endcodeblock %}