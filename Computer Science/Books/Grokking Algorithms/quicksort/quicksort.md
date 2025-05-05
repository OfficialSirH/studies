[[quicksort]]

## Explanation

### Partitioning

Choose a pivot point and find all elements that are less than the pivot and the elements that are greater than the pivot. This will leave you with the sub array of smaller elements, the pivot, and the sub array of larger elements.

### Base Case

If there are 0 or 1 elements, it's done, if 2, you simply swap them if necessary.

### Recursive Case

If there are still sub arrays to be sorted, continue them with pivots until they reach base case.

## Notes

- Divide & conquer are recursive algorithms that are solved as such:
	1. Figure out the base case. This should be the simplest possible case.
	2. Divide or decrease your problem until it becomes the base case.
- Euclid's algorithm: "If you find the biggest box that will work for this size, that will be the biggest box that will work for the entire farm."
- single or no element arrays are base case.
- quicksort's big O is only on average O(n log n) while merge sort is always O(n log n), making it technically faster but slower in terms of constant.

## Exercises

- 4.1 Write out the code for the earlier `sum` function.
```ts
function sum(arr: number[]): number {
	if (arr.length === 1) {
		return arr.pop();
	}
	return arr.pop() + sum(arr);
}
```
- 4.2 Write a recursive function to count the number of items in a list.
```ts
function countItems(arr: number[]): number {
	let item = arr.pop();
	if (item === undefined) {
		return 0;
	}
	return 1 + countItems(arr);
}
```
- 4.3 Find the maximum number in a list.
```ts
function findMax(arr: number[]): number {
	let item = arr.pop();
	if (item === undefined) {
		return item;
	}
	let secondItem = findMax(arr);
	return item >= secondItem ? item : secondItem;
}
```
- 4.4 Remember binary search from chapter 1? It’s a divide-and-conquer algorithm, too. Can you come up with the base case and recursive case for binary search?
```ts
// base case: is the number or no numbers left to search
// recursive case: not the number that is being searched for
function binarySearch(arr: number[], value: number, lhs = 0, rhs = arr.length - 1): boolean {
	let index = (lhs + rhs) / 2;
	let item = arr[index];
	if (item == value) {
		return true;
	}
	if (lhs === rhs) {
		return false;
	}
	if (item < value) {
		lhs = index;
	} else {
		rhs = index;
	}
	return binarySearch(arr, value, lhs, rhs);
}
```

How long would each of these operations take in Big O notation?
- 4.5 Printing the value of each element in an array.
O(n)
- 4.6 Doubling the value of each element in an array.
O(n)
- 4.7 Doubling the value of just the first element in an array.
O(1)
- 4.8 Creating a multiplication table with all the elements in the array. So if your array is `[2, 3, 7, 8, 10]`, you first multiply every element by 2, then multiply every element by 3, then by 7, and so on.
O(n^2)