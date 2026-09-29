# Stacks and Queues

## Stacks 

Stacks are a type of collection which follow the 'FIFO' rule for insertion and removal of elements. They highly standardised:
- Typically, they are homogenous and therefore can only have one type of data. 
- There are usually three operations: `push`, `pop`, `peek`
- There are sometimes auxiliary operations, like `clear`, `size` / `length` and other similar operations.
### FIFO 

'FIFO' stands for 'First-In-First-Out', which means that they only allow removal of the most recently inserted element, functioning exactly like a physical stack of books. Strictly speaking, no other elements are accessible or visible. 

This puts limitations on how these collections can actually be used. They cannot be treated like typical lists or arrays, but this structure makes them quite useful for any application which requires elements not to be processed in discovery order, and where processing can lead to discovery. 
### Semantics

While it doesn't always reflect the underlying implementation, stacks are usually visualised (as the name suggests) as a physical stack. This also relates to how we talk about them. 

The *'bottom'* of the stack is the region(s) of memory where the  oldest elements are stored. The *'top'* is the region where the most recently inserted elements are stored. In the same vein, *'higher'* elements are more recent. 
### Operations
- `pop` : Remove the top element and return it
- `push`: Add an element to the top
- `peek`: show the top element, but do not remove it or allow mutation
- `length`
- `clear`
### Applications
**TODO**
## Implementation
**TODO**