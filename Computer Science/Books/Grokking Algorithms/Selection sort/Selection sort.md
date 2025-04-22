[[Grokking Algorithms]]

## Explanation

The sorting is done by checking for what element fits the condition (commonly largest/smallest value if sorting numbers) then adds it to the new array. This is done repeatedly until all elements have been added into the new array and therefore gives a fully sorted array.

Due to the algorithm constantly reiterating over all the elements to find the next element that fits the next slot, this makes the algorithm $O(n^2)$
