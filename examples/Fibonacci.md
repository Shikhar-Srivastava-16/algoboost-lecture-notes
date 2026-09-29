The fibonacci series is the series of numbers formed by adding together the last two existing numbers to add an element. It starts with (0, 1) and continues like this: 
![[fibonacci.svg]]

In an expressive sense, this series breaks down to something of following description. Ignore the fact that the the code blocks say they're rust - they have a nasty habit of trying to trick you.


The nth number in a fibonacci series becomes this:
```Rust
fibonacci(0) = 0   // 0th member is 0
fibonacci(1) = 1   // 1st member is 1

// nth member is the sum of the member before it and the member before that, 
// so, the sum of the (n-1)th and (n-2)th member

fibonacci(n) = fibonacci(n-1) + fibonacci(n-2) 
```

Consider again the fibonacci sequence. It is a list, defined as a pattern, and the only thing immediately obvious in a programmatic sense is that it is constructed by some sort of repeated operation. 

On observation, a few more things become evident:
- Everything that we need to construct the series *ad infinitum* (and beyond!) is contained within the list
- We can start at any length and end at any length
- This looks like a prime candidate for recursion:

```Python
# here's a python function that constructs a fibonacci series of length n

def fib_memo(length: int):
    if length == 1:
	    return [0]
    
    if length == 2:
        return [0,1]
	
	pre = fib(length-1)
    return pre + [(pre[-1] + pre[-2])]

# Try it out yourself!
# Try and print the list at every step to see the steps it follows
```

We're *almost* there. Recursion is a nice way to look at these programs and a very useful style of programming. Dynamic Programming is a generalisation of recursion, and often, recursive functions can be seen as a way of performing dynamic programming. 

Another way of looking at the fibonacci sequence is that calculating any element is trivial if all previous values are known. 

The 'next' number from a list is:
```Rust
// ++ is the notation I have used for concantenation of lists
// nums is a (possibly empty) list that already follows the fibonacci sequence

// 
fibonacci_next(nums ++ [num1] ++ [num2]) = 
	nums ++ [num1] ++ [num2] ++ [(num1+num2)]
```

Notice that it is really quite easy to define any number in terms of each of the preceding numbers. If we do this 'recursively', we end up with the following (absolutely abysmal) sequence being simplified under the hood:

```
0, 1, 0+1, 1+(0+1), (0+1)+(1+(0+1)) ...
```

This is actually on the right track, because we have now broken the larger problem into a number of smaller, recurring problems, which then get solved one after the other. This is the common thread between recursion and dynamic programming. The difference between the two is the information which is accessible at any time. Recursion works by expressing problems in terms of successive, smaller problems. Dynamic Programming works by expressing problems as nested problems. 

With recursion, we build an expression that writes itself by copying sub-expressions. With DP, we write an expression that is built using unknown data, which gets filled in 'dynamically', or while running the program. 

There is more trickery involved here -  techniques like caching and memoisation are used to make the solutions of sub-problems available at runtime instead of recalculating them as with recursion. 