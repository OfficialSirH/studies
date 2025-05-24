[[Grokking Algorithms]]

## Hash functions

Hash functions are functions that are used to turn a string (or slice of bytes) into a value, that value being the index for where that string will point to in a hash table. These functions work through ensuring they produce the same value every time for the same string but always a unique number for every different string so each string may have their own index.

### Exercises

Which of these hash functions are consistent?
- 5.1 `f(x) = 1` <- Returns "1" for all input
	- This is technically consistent since the same input will give the same output, but it's not consistent as all input gives the same output.
- 5.2 `f(x) = rand()` <- Returns a random number every time
	- This is not consistent because same input will almost always give a different output and other inputs could potentially get the same output as another input.
- 5.3 `f(x) = next_empty_slot()` <- Returns the index of the next empty slot in the hash table
	- This is not consistent because same inputs will always get a different output.
- 5.4 `f(x) = len(x)` <- Uses the length of the string as the index
	- This is partially consistent as inputs with different lengths will get different outputs, same inputs will get the same output but has major flaws when it comes to different inputs with the same length.

## Use cases

Hashing is great for making servers more efficient via caching as your static pages that stay the same and may be viewed a lot can be stored to always show the same content every time it's requested so then the server doesn't need to generate it every time it's requested. Hash tables can also be compared to memory as the more you're asked similar questions, the easier it is for you to recall the answer as you slowly map the question to the answer. Another great use case is for ensuring duplicates don't arise by keeping track when a certain input has already been received and then ignoring it.

## Collisions

Collisions are what happen when different inputs give the same output, which aren't ideal but over larger sets of data become inevitable. The best way to reduce collisions is to ensure your **hash function** is best curated for your dataset by aiming to evenly spread out the outputs over the whole array. The second way to avoid collisions is with a low **load factor**, which should looking something like **0.7** or lower and the size of the array should be **double the amount of items** within the hash table. If the load factor gets too high, you need to *resize* the array so the items may get more evenly spread out.

### Load Factor

$$
\frac
{\text{Number of items in hash table}}
{\text{Total number of slots}}
$$

### Exercises

Suppose you have these four hash functions that work with strings: 
- A. Return “1” for all input. 
- B. Use the length of the string as the index. 
- C. Use the first character of the string as the index. So, all strings starting with a are hashed together, and so on. 
- D. Map every letter to a prime number: a = 2, b = 3, c = 5, d = 7, e = 11, and so on. For a string, the hash function is the sum of all the characters modulo the size of the hash. For example, if your hash size is 10, and the string is “bag”, the index is 3 + 2 + 17 % 10 = 22 % 10 = 2. 

For each of these examples, which hash functions would provide a good distribution? Assume a hash table size of 10 slots. 
- 5.5 A phonebook where the keys are names and values are phone numbers. The names are as follows: Esther, Ben, Bob, and Dan. 
	- Utilizing [[#Letters to Prime Numbers]], the following values would be mapped to each name: 
		- Esther would output 0 as their accumulated primes equals 240, then modulo 10 would equal 0.
		- Ben would output 7 from 47 % 10.
		- Bob would output 3 from 53 % 10.
		- Dan would output 2 from 52 % 10.
		Therefore hash function D would give the best results as the inputs have 0 collision.
- 5.6 A mapping from battery size to power. The sizes are A, AA, AAA, and AAAA.
	- Both hash functions, B and D, would work best for this as they both have 0 collisions. They would be distributed as the following:
		- B: 1, 2, 3, 4
		- D: 2, 4, 6, 8
- 5.7 A mapping from book titles to authors. The titles are Maus, Fun Home, and Watchmen.
	- C is right away a contender as it has 0 collisions for all 4 titles as they all have different letters in the start of them, but just to be sure, let's utilize the [[#Letters to Prime Numbers]] for D:
		- Maus would output 3 from 183 % 10.
		- Fun would output 9 from 129 % 10.
		- Home would output 8 from 118 % 10.
		- Watchmen would output 5 from 275 % 10.
		This confirms that D also works as there are 0 collisions with these 4 inputs, so both C and D work for this case.

### Letters to Prime Numbers

A = 2
B = 3
C = 5
D = 7
E = 11
F = 13
G = 17
H = 19
I = 23
J = 29
K = 31
L = 37
M = 41
N = 43
O = 47
P = 53
Q = 59
R = 61
S = 67
T = 71
U = 73
V = 79
W = 83
X = 89
Y = 97
Z = 101