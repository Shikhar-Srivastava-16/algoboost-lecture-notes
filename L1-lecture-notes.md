# Lecture 1: Introduction

## Why do we need Data Structures and Algorithms

### Data Types:
Most programming languages store data in variables that have 'types'. This can broadly be divided into the following categories: 
- **Primitive Data Types**: Those types which can be stored directly:
	- Integers: represented as Decimals, Binary or Hexadecimal. Usually stored in binary.
	- Booleans: 0 or 1 => False or True, respectively. Stored as a single switch
	- Chars: just integers, with an [ASCII](https://www.ascii-code.com/) encoding
- **Dependent Data Types:** Everything else! More complicated information can be stored by decomposing it into multiple instances of primitives. For example, even simple data like a String actually contains a list of chars: the word "AlgoBoost" would actually be `[ A, l, g, o, B, o, o, s, T ]` , which is a List of `char`(s). 
  To store values of these dependent data types, we need *Data Structures* and in order to conduct operations on these value, we need *Data Structure Algorithms*. In the previous example, the data structure would be some type of list. 
### Data Structures:
Common Data Structures include:
- Linked Lists: A collection of Nodes, which consist of a *value* and a *next pointer* which goes to the next node.
- Trees: A collection of Nodes, each with 1 or more Child Nodes.
- Graphs: A collection of Nodes, linked to each other in any configuration with edges
- Arrays: A contiguous block in memory, which is indexed using numbers and reserved only for use within the array. 
- Stack and Queues, which enforce specific Insertion and Removal orders
- Common Mathematical Structures: Sets, Matrices and so on.

These end up being used either to store complex data, such as **Strings** and so on. We will cover all of this in detail in later DSA talks. 

Data Structures often feature heavily in technical Interviews and questionnaires, so it is useful to understand how to use them, practice common problems and to be able to answer questions about them. 

## Answering DSA Questions

During our talks, we will be covering how to work with data structures, how to solve common problems and practicing these concepts. It is important to keep in mind that we will be building towards three common things during these lectures.

### Working with Data Structures

Data Structure Algorithms are a way of working with different Data Structures. During this lecture series, we will first go over the mechanical details of Data Structures and then over common techniques used in Algorithms. This should help you learn how to solve the most basic problems. 

These basics can then be combined to solve larger and larger problems.
### Computational Thinking
The problems that you are looking to solve will almost never be a problem which you have memorised and learned a solution to. However, it will almost always be a problem which can be broken down into smaller parts, which will then get closer to problems which you already know how to solve. 

For example: 
*You have been given a table that has cubes, their sizes, and the material which they are each made out of. Find the median weight of these cubes.*

There is no single algorithm or procedure to do this. However, we know how to calculate weight using volume and density. We know how to take those weights and sort them. We also have algorithms that can find the median of a sorted list.

This practice of taking a complex problem that we do not know how to solve, and breaking it down into simpler problems which we know how to solve is known as ***Computational Thinking***

### Dynamic Programming
Dynamic programming is the practice of taking a large problem, then breaking it into repeating instances of a known problem is called *Dynamic Programming*. Keep this definition in mind, we shall build up to it and go over this topic again at the end of the series. 

### Practice!
The best way to get into the routine of solving these problems is to solve lots of them, while knowing the structure of the problems on which you are working, and the Data Structures with which you are working on them. For this, we recommend using the following resources regularly:

#### [Hackerrank](https://www.hackerrank.com/)
Contains problems that will require you to use the pattern and algorithms that you have learned. These sometimes include full-blown APIs and implementing things that you might actually need to implement in the workplace. 

Hackerrank is a great way of understanding that the problems that you are faced with will often have solutions that do not involve any data structure algorithms, but quite often you will be able to use the techniques we go over in order to come up with better solutions, and do so quicker. 
#### [LeetCode](https://leetcode.com/)
Leetcode contains a lot of good statement-style problems that you should be able to solve by applying some of the algorithms and techniques we will go over, or using a small modification of these algorithms.
#### [NeetCode](https://neetcode.io/)
Neetcode is a tool that teaches the implementation of data structures, often in very low-abstraction languages such as C. This is also useful, for two reasons:
- Such problems show up in interview questions and technical sections
- Having a working understanding of the way these data structures are implemented is important when thinking about ways to write and optimise solutions

## General Recursion

### Recursive Functions

A recursive function is one which calls itself to perform repeated tasks. Recursive functions generally operate on Recursive Data Structures like **Graphs, Trees and Linked Lists**(more in subsequent talks) which mirror this repetition in their composition.

All useful recursive functions have at least one 'base case' and one recursive case. The recursive case is responsible for repetitive actions by calling the function again and again. The base case or cases will halt this repetition. If there is no base case, the function repeats forever until there is an external problem like an error, or a stack overflow or something similar.  

When these functions get called *once* in the code, there are usually multiple function calls. This forms what a 'call graph', which is a very useful way of visualising recursion. You can visualise the call tree for functions that you write on a website called [RecurSee](https://recursee.com/). If you want to see why memoised functions are better, compare the two variants of the recursive `fib` function on this tool.

The classic example of Recursion is a function that generates the nth element of the [Fibonacci Sequence](https://en.wikipedia.org/wiki/Fibonacci_sequence). 

```Python
# This is a function that generates the nth element of the fibonacci sequence
def fib(n):
	if n <= 1:
		return n
	
	return fib(n - 1) + fib(n - 2)
```
### Memoisation

One of the big problems with recursion is that it leads to a massive number of calls, which leads to a number of recalculations. For instance, in the fibonacci example, to calculate each element in the series, you also recalculate every single other element. 

This is a bad idea, because it is often significantly faster to store those elements and then access them in storage later on. **Memoisation** is an optimisation on recursion that involves storing all useful values that we have calculated, instead of letting them go out of access.

There is some flexibility in the way that these elements are stored, but generally memoising stores computed results in something like a dictionary or a map, and then references it again and again. 

Here is an example of the same result being produced using a memoised solution:

```Python
def fib(n):
	fib_in(n, [0,1])

# internal helper function so that we don't keep having to pass the memo dictionary in everytime we call the function in code
def fib_in(n,memo):
	if n < len(memo):
		return memo[n]
	
	memo += [fib_in(n - 1, memo) + fib_in(n - 2, memo)]
	return memo[n]
```

Note how the `memo` dictionary is tracked by passing it as an argument repeatedly  rather than relying on global scope. This is considered good practice, largely because these values get used only during a single recursive 'run' of this function. 

If it were scoped globally, every time a new function uses it, it would have to be reset over and over again. This means that programmers have more and more things to keep track. Since there is no real benefit to having a global `memo` array, it is a good idea to sidestep this problem entirely. 

Having familiarised yourself with this function in both the optimised and basic variants, you should attempt to build the recursive and memoised versions of the following function in python (or any other language you want!):

```Python
'''
fib_list(n) is a function that takes in an integer 'n' and returns a list
the list returned should have the first n elements of the fibonacci sequence
'''
def fib_list(n):
	# placeholder
	pass
```