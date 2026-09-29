## From WICSxAlgoboost: Special Fibonacci Sequence
### Problem:

```
A fibonacci sequence is a list of integers, starting with `[0,1]`. Every subsequent element is the sum of the two preceding numbers.

A *special* fibonacci sequence in the context of this question is one whose first two elements are not fixed, and which uses a special operation (which we shall call `sp_add`). 

Assuming that the initial elements provided will always be valid, and that sp_add will be O(n) just like regular addition; write a function that can compute a special fibonacci sequence. 

Once you have a recursive algorithm, can you develop a faster solution?

Hint: try using memoisation
```

The problem here is explicitly dealing with a Fibonacci Sequence generation algorithm which has a few special characteristics. In problems that are either explicitly, or implied to be, 'special' versions of a common or well-known DSA problem, I find t useful to first start with a list of the 'special' characteristics that the problem statement demands.

In this case, that would be a Fibonacci Sequence problem 