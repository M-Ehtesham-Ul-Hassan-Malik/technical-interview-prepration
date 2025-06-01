
## What is a stack?
A stack is a linear data structure that follows the **Last In First Out** (LIFO) principle.
For example stack of plates in kitchen.

## What are the operations performed on a stack?
The common operations performed in stack are:
- push() : Adds an item on the top of the stack
- pop() : Removes and returns the top item
- peek() : Returns the top element without removing it
- isEmpty() : Checks if the stack is empty
- size() : Returns the number of elements in the stack

## What is the time complexity of stack operations?
- push(): O(1)
- pop() : O(1)
- peek() : O(1)
- isEmpty() : O(1)
- size() : O(1)

##  What is the time complexity of inserting an element at the bottom of a stack?
To insert the element at the bottom of stack we need to 
- pop all the element and store them temporarily `O(n)`
- insert element `O(1)`
- push all the stored elements back in reverse order `O(n)` <br>

so the overall time complexity O(n)

## What are the applications of a stack?
Stack used in many programming scenarios:
- Backtracking algorithms e.g: maze solving, N-Queen problem etc
- Reversing data e.g: reversing array or string etc
- Depth-First Search(DFS) uses stack to explore graph paths deeply
- Recursion and many nested function calls

## What is a stack overflow?
Stack overflow occurred when the stack exceeds its allocated memory.

## What is a stack underflow?
when the stack is empty and someone attempts to pop an element



## References
- [geeksforgeeks](https://www.geeksforgeeks.org/commonly-asked-data-structure-interview-questions-on-stack/)
- [chatgpt](https://chatgpt.com/)