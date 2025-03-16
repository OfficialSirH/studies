
## Explanation

The process of always checking the middle between 2 bounds, starting with the list's beginning and ending bounds, then adjusting those bounds to whether the checked value was too high or too low.

## Visual

Say you have to guess a number between 1 - 1000 and the number is 337, this is how it'd look if you checked each individual value from start to end:
`1, 2, 3, 4, 5, 6, ...` (337 guesses)
With binary search:
`500, 250, 375, 313, 344, 328, 336, 340, 338, 337` (10 guesses)

## Exercises

1. Suppose you have a sorted list of 128 names, and you’re searching through it using binary search. What’s the maximum number of steps it would take?

it would take 7 steps. $\log_{2}(128) = 7$

1. Suppose you double the size of the list. What’s the maximum number of steps now?

it would then be 8 steps. $\log_{2}(256) = 8$
