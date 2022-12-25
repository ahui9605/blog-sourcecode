---
title: Huffman Algorithm and Greedy Method
date: December 17, 2022
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

description: ITS495 Special Topics Huffman Coding Algorithm
---

### Introduction

A specific kind of optimum algorithm called a Huffman code is frequently employed for lossless data compression in computer science. This is a method created by David A. Huffman while he was a Sc.D. student at MIT, is used to find or use such a code. It was first published in the 1952 publication "A Method for the Construction of Minimum-Redundancy Codes."

Huffman's approach produces what is essentially a variable-length code table for encoding a source symbol (such as a character in a file). The estimated frequency of occurrence for each potential value of the source symbol is what the algorithm uses to create this table. Commoner symbols are typically represented using fewer bits than less common symbols. If the inputs are sorted, Huffman's approach can be applied quickly, discovering a code in a time that is proportional to the number of inputs. Even though it is not the best compression method, it was released in 1952, making it a fairly algorithm that was widely used in specific research purpose or commercial purpose such as WinZip compression tool and JPEG, PNG picture format.

### Step by Step Explanation

#### Read file from source and extract

In order to describe the Huffman method in detail, step by step, I used the programming language Python. Note that this is not the greatest way for optimizing these codes such that they can take up more space and need more time to encode. This paper is just to explain how Huffman coding works.

First, In the Figure 1.1, I made a new text file. I want Python to read the strings in ASCII format. And put all of the information in the txt file to a variable: {% label my_string blue %}. I need to get the total length of the code to do the next step.
{% codeblock lang:python %}
file = open("data.txt", "r", encoding="ascii")
my_string = file.read()
len_my_string = len(my_string)
#Figure1.1: Ask python to read the txt file named data.txt and put all information in a new string called my_string and get its length
{% endcodeblock %}

Because the text file contains more than 2,700 characters, I will use the short string as an example(Figure1.2) in this paper.
{% codeblock lang:python %}
my_string = "ahwderghs"
#Figure 1.2: Using this variable my_string as an example in paper
{% endcodeblock %}

#### Count letters

We need to find some of the unique letters. We don’t want to store lots of duplicated letters in a new array list. Also, I used a {% label count() blue %} built-in Python function, which allows me to count how many times they appear in my string(Figure 2.1).

{% codeblock lang:python %}
letters = []
only_letters = []
for letter in my_string:
if letter not in letters:
freq = my_string.count(letter)
letters.append(freq)
letters.append(letter)
only_letters.append(letter)
#Figure 2.1: A code block of checking the unique letters and their frequently
{% endcodeblock %}

#### Build leafs and nodes

After we get all the letters count and unique letters in the arrays, we start to build the Huffman tree (Figure 3.1), where we need to have some nodes. Make sure to order the tree in ascending order after adding all of the nodes huffman_tree[] array will be used as the final tree, and the nodes array will be used to combine and merge.

{% codeblock lang:python %}
nodes = []
while len(letters) > 0:
nodes.append(letters[0:2])
letters = letters[2:]
nodes.sort()
huffman_tree = []
huffman_tree.append(nodes)
#Figure 3.1: A code block of building a Huffman Tree base and their nodes
{% endcodeblock %}

This is a recursive function (Figure3.2) to repeat the call to build the tree from the root all the way to the last leaf. Make sure it is in ascending order before starting to build. We want to ensure the two nodes are the smallest as the Huffman algorithm is a greedy method. We need to make sure all the things are the best optimized.

Let's take the {% label nodes[pos] blue %} as the left nodes and {% label nodes[pos+1] red %} as the right nodes. And we want to append other elements.

{% note modern %}
For example, the {% label "node[pos] = [1, ‘a’, 0]" blue %} as the left side. The {% label "node[pos+1] = [2, ‘h’, 1]" red %} is the right side. Take them as the binary codes 0 and 1.
{% endnote %}

{% codeblock lang:python %}
#this is a recursive function that combines all the letters with the frequency count for each of those letters. It will keep recurse until the length of the nodes is less than 1.
def combine(nodes):
pos = 0
newnode = []
if len(nodes) > 1:
#before each iteration of the recursive process, we have to check that the nodes are arranged in ascending order.
nodes.sort()
#We add 0 and 1 on each node, where the first node (located on the left side) is 0, and the second node (located on the right side) is 1.
nodes[pos].append("0")
nodes[pos + 1].append("1")
#we start to combine the nodes. for example: nodes = [[1,"a"],[2,"h"]]
#we combine the first and the second nodes of its elements together. Their frequently count number combine together: 1 + 2 =3
combined_node1 = nodes[pos][0] + nodes[pos + 1][0] # we combine the first and second nodes of its letter, which is "a" and "h" combined to form "ah."
combined_node2 = nodes[pos][1] + nodes[pos + 1][1] # We create a new node by combining these two existing nodes into a single one. We store newly created nodes in the newnode[]. newnode = [3, "ah"]
newnode.append(combined_node1)
newnode.append(combined_node2)
#we are now adding the new nodes together with the rest of the nodes that we haven't used before. We should also need to remove the old nodes that were combined earlier.
#it will end up looking something like this: [[3, "ah], [3,"g"], [5, "s"]...] The first element (node) is the newly combined node that we just completed. and the remaining ones make up the older nodes.
newnodes = []
newnodes.append(newnode)
newnodes = newnodes + nodes[2:]
#after that, update the nodes with the new nodes, which are [3, "ah"] as well as those old nodes. This is going to be used once more for the subsequent recrusive.
nodes = newnodes
huffman_tree.append(nodes)
#recursion will be called again until the nodes[] is less than 1
combine(nodes) # after the recursion is done, return to the huffman_tree with different nodes combined together
return huffman_tree
#call this recursion funciton to recurse the nodes[]
newnodes = combine(nodes)

#Figure 3.2: A code block of a recursive function to be called to combine nodes in Huffman Tree
{% endcodeblock %}

#### Tree built but need revision

Then we start to combine these two nodes with the least values in the huffman_tree array. So it will become something like this: {% label "newnode = [3, ‘ah’]" blue %}. Then we keep combining and combining again until the length of the {% label "newnode[]" blue %} has one element left. The, we return to the final Huffman tree.

![](/images/Algorithm/Huffman_Tree_Unreverse.png "Figure 3.3: Example of what the Huffman tree looks like after combing.")

This is what the final tree looks like, but in Figure 3.3, it doesn’t seem correct because the tree root should be at the top where those leaves are supposed to be at the bottom. So we need another built-in python function to reverse the whole tree (Figure 3.5).

{% codeblock lang:python %}
huffman_tree.sort(reverse=True)
{% endcodeblock %}

![](/images/Algorithm/Huffman_Tree_Reversed.png "Figure 3.5 Reversed sorting Huffman tree")

#### Remove Duplicated elements

However, we noticed lots of duplicated elements in the tree (Figure 3.5) where the Huffman tree does not accept duplicated nodes in the tree same as the Binary Search Tree algorithm. So, we need to remove those redundant elements.

{% codeblock lang:python %}
checklist = []
for level in huffman_tree:
for node in level:
if node not in checklist:
checklist.append(node)
else:
level.remove(node)

#Figure 3.6: Remove duplicated element algorithm
{% endcodeblock %}

After we remove those duplicated elements by using an algorithm in Figure 3.6, we can move forward and encode those English letters into binary code. In figure 3.7, the loop will check if the targeted letter exists in each node. If the letter exists in these nodes, it will note them down; if the letter does not exist in these nodes, it will note down an empty value: “” with nothing inside the quotation marks.

{% codeblock lang:python %}

#after that, we begin the process of converting these letters into our own unique binary code using the shortest amount of space possible (greedy method)
letter_binary = []
if len(only_letters) == 1:
letter_code = [only_letters[0], "0"]
letter_binary.append(letter_code \* len(my_string))
else: # this will check to see if the letter contains each of the nodes and then proceed accordingly. In the event that it does contain, add the binary value of the nodes, which can be found in the third position of the index. # If it does not contain anything, simply add the character sequence "" which is a string empty of any content and enclosed in quotation marks.
for letter in only_letters:
lettercode = ""
for node in checklist:
if len(node) > 2 and letter in node[1]:
lettercode = lettercode + node[2]
letter_code = [letter, lettercode]
letter_binary.append(letter_code)

#Figure 3.7: Converting the letters to binary codes by using the Huffman tree.
{% endcodeblock %}

#### Get our own ASCII table and binary codes

Now we get a table with Huffman algorithm, use this array and its element to convert our English text to the binary code. Converting algorithm can be seen below:
{% note modern %}
[['a', '1110'], ['h', '01'], ['w', '110'], ['d', '1111'], ['e', '000'], ['r', '100'], ['g', '001'], ['s', '101']]
{% endnote %}

#### Encoding by using our own ASCII table

{% codeblock lang:python %}
bitstring = ""
for character in my_string:
for item in letter_binary:
if character in item:
bitstring = bitstring + item[1]
{% endcodeblock %}

#### Get the encoded string

Then we get a binary code with a very short length. Compared to the file size with ASCII table size is 72 bits, and we compressed it to the size of 27 bits. The size is reduced to 62% which is a very efficient algorithm to use.

{% note modern %}
111001110111100010000101101
{% endnote %}
