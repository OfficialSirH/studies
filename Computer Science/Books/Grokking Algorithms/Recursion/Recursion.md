[[Grokking Algorithms]]

## Notes

- Recursive functions can make solutions clearer while normal loops can be more performant
- Recursive functions have 2 parts, the *base case* and the *recursive case*. the recursive case is the case where the function calls itself and the base case is the one that tells the function when to stop
- A stack has only 2 actions, push (adding an item to the top of a list), and pop (removing and reading an item on the top of the list)
## Exercises

- Suppose you’re digging through your grandma’s attic and come across a mysterious locked suitcase. Grandma tells you that the key for the suitcase is probably in this other box. Tis box contains more boxes, with more boxes inside those boxes. The key is in a box somewhere. What’s your algorithm to search for the key?

iterating through each box, you search for a key, if the key isn't in the current box, go to the next box and search for the key there, and repeat until the key is found.

- (Look at image of call stack in 3.1) What information can you give me, just based on this call stack?

There's a function called "greet" that is called with "maggie" as a parameter named "name" and then within that function, a function called "greet2" is called with "maggie" as well with the same parameter name.

- Suppose you accidentally write a recursive function that runs forever. As you saw, your computer allocates memory on the stack for each function call. What happens to the stack when your recursive function runs forever?

- The computer runs out of memory and crashes the program