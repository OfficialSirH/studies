[[Grokking Algorithms]]

## The knapsack problem

The knapsack problem again, but in this example the thief only is able to carry 4 lbs of goods. Three items to choose from:
- Stereo - $3000 - 4 lbs
- Laptop - $2000 - 3 lbs
- Guitar - $1500 - 1 lbs
How would you gather the maximum value of goods effectively?

### The simple solution

The simplest way to go about this is to iterate through all possible combinations of items that can be gathered to find the one that fits the weight criteria and has the highest value. The problem with this is that for each item more, it doubles, making it take O(2^n), which is far from ideal. Another way of going about this problem is through approximation, but that usually only gets *near* the optimal solution rather than at the optimal solution, so how would you calculate the optimal solution?

### Dynamic programming

With dynamic programming, calculating the optimal solution should become trivial. This is done by breaking down the problem into subproblems and through these subproblems, the main problem can be solved. This starts with a grid, like below:

|        | 1       | 2       | 3       | 4         |
| ------ | ------- | ------- | ------- | --------- |
| Guitar | $1500 G | $1500 G | $1500 G | $1500 G   |
| Stereo | $1500 G | $1500 G | $1500 G | $3000 S   |
| Laptop | $1500 G | $1500 G | $2000 L | $3500 L G |

Filling in this grid, you figure out that the Laptop and Guitar combined have the greatest value, which is calculated by getting the maximum value between the previous max vs the combination of the value of the current item and the value of the remaining space.

```
					
					1. The previous max (value at cell[i-1][j])
cell[i][j] max of {
					2. Value of current item + value of the remaining space cell[i-1][j- item's weight]
```

## Knapsack problem FAQ

### What happens if you add an item?

When a new item is added, you simply just create a new row in the grid for it, as the previous values are of the previous maximums and therefore has no confliction to just add a new item afterwards to check for a new maximum.

- Iphone - $2000 - 1 lbs

|        | 1       | 2         | 3         | 4         |
| ------ | ------- | --------- | --------- | --------- |
| Guitar | $1500 G | $1500 G   | $1500 G   | $1500 G   |
| Stereo | $1500 G | $1500 G   | $1500 G   | $3000 S   |
| Laptop | $1500 G | $1500 G   | $2000 L   | $3500 L G |
| Iphone | $2000 I | $3500 I G | $3500 I G | $4000 I L |

As you can see, with the new item, it creates new maximums without any issues.

Question: Would the value of a column ever go *down*? Is this possible?
No, it wouldn't be possible as the maximums always seek for higher valued combinations and never goes for items that could give a lower valued combination.

### Exercise

- 9.1: Suppose you can steal another item: an MP3 player. It weighs 1 lb and is worth $1,000. Should you steal it?
	- Yes, because of its light weight and decent value, it's able to be included into the largest knapsack along with the guitar and Iphone, giving a slight increase in our final maximum:
	
|            | 1       | 2         | 3         | 4           |
| ---------- | ------- | --------- | --------- | ----------- |
| Guitar     | $1500 G | $1500 G   | $1500 G   | $1500 G     |
| Stereo     | $1500 G | $1500 G   | $1500 G   | $3000 S     |
| Laptop     | $1500 G | $1500 G   | $2000 L   | $3500 L G   |
| Iphone     | $2000 I | $3500 I G | $3500 I G | $4000 I L   |
| MP3 Player | $2000 I | $3500 I G | $3500 I G | $4500 I G M |

### What happens if you change the order of the rows?

Nothing as the maximums will always reach the same value every time as the combinations are all tested through maximum comparisons.

|        | 1       | 2       | 3       | 4         |
| ------ | ------- | ------- | ------- | --------- |
| Stereo | 0       | 0       | 0       | $3000 S   |
| Laptop | 0       | 0       | $2000 L | $3000 S   |
| guitar | $1500 G | $1500 G | $2000 L | $3500 L G |

### What happens if you add a smaller item?

If an item like a necklace of 0.5 lbs were added, the grid would have to be adjusted for the higher granularity and would look something like this:

|          | 0.5 | 1   | 1.5 | 2   | 2.5 | 3   | 3.5 | 4   |
| -------- | --- | --- | --- | --- | --- | --- | --- | --- |
| Guitar   |     |     |     |     |     |     |     |     |
| Stereo   |     |     |     |     |     |     |     |     |
| Laptop   |     |     |     |     |     |     |     |     |
| Jewelery |     |     |     |     |     |     |     |     |

### Can you steal fractions of an item?

This can't be done with the dynamic-programming solution as it infers you take it all when you take something, but this can be done with a greedy algorithm. For example, if you have three items to choose from:
- Quinoa - $6/lb
- Dal - $3/lb
- Rice - $2/lb
You just go with the highest valued item until it's empty, go for the next one, and go until you're too full to carry more of them.

### Optimizing your travel itinerary

You want to see as many places as possible in London, you've ranked them based on how much you want to see them and also wrote how much time each one takes:
- Westminster Abbey - 1/2 Day - 7
- Globe Theatre - 1/2 Day - 6
- National Gallery - 1 Day - 9
- British Museum - 2 Days - 9
- St. Paul's Cathedral - 1/2 Day - 8

|                  | 1/2 | 1      | 1 1/2    | 2        |
| ---------------- | --- | ------ | -------- | -------- |
| Westminster      | 7 W | 7 W    | 7 W      | 7 W      |
| Globe Theatre    | 7 W | 13 W G | 13 W G   | 13 W G   |
| National Gallery | 7 W | 13 W G | 16 W N   | 22 W N G |
| British Museum   | 7 W | 13 W G | 16 W N   | 22 W N G |
| St. Paul's       | 8 S | 15 S W | 21 S W G | 24 W N S |

### Handling items that depend on each other

If you had a problem that deals with values that adjust based on others, like times for visiting locations adjusting based on if you went to one of them. This problem can't be solved with dynamic programming as it depends on discrete subproblems- problems that don't depend on each other.

## Is it possible that the solution will require more than two sub-knapsacks?


Due to how the algorithm works, you only deal with two sub-knapsacks, but it's possible for the knapsacks to hold knapsacks as to allow for more than 2.

### Is it possible that the best solution doesn't fill the knapsack completely?

Yes, a valuable (or combination of valuables) could potentially add up to the highest maximum in a problem but not fill up the bag if there's no items that are light enough to fit within the leftover space.

### Exercise

- 9.2: Suppose you’re going camping. You have a knapsack that will hold 6 lb, and you can take the following items. Each has a value, and the higher the value, the more important the item is: 
	- Water, 3 lb, 10 
	- Book, 1 lb, 3 
	- Food, 2 lb, 9 
	- Jacket, 2 lb, 5 
	- Camera, 1 lb, 6 
What’s the optimal set of items to take on your camping trip?

The optimal set of items would be:
- Camera
- Food
- Water

|        | 1   | 2   | 3      | 4        | 5      | 6        |
| ------ | --- | --- | ------ | -------- | ------ | -------- |
| Water  | 0   | 0   | 10 W   | 10 W     | 10 W   | 10 W     |
| Book   | 3 B | 3 B | 10 W   | 13 B W   | 13 B W | 13 B W   |
| Food   | 3 B | 9 F | 12 F B | 13 B W   | 19 F W | 22 F B W |
| Jacket | 3 B | 9 F | 12 F B | 13 B W   | 19 F W | 22 F B W |
| Camera | 6 C | 9 F | 15 C F | 18 C F B | 19 F W | 25 C F W |

## Longest common substring

Say you're trying to guess what word a user is trying to type when querying dictionary.com, the user gave *hish*, the 2 possibilities given are *fish* and *hish*, how do you compare their relation? We can compare the substrings of both *fish* and *hish* to see how closely related they are in value with a grid:

|     | H   | I   | S   | H   |
| --- | --- | --- | --- | --- |
| F   | 0   | 0   | 0   | 0   |
| I   | 0   | 1   | 0   | 0   |
| S   | 0   | 0   | 2   | 0   |
| H   | 0   | 0   | 0   | 3   |

With the above grid, the value is based on the previous row and column cell + 1, leading to the final value being 3 for the substring length. Now if we compare *vista* as well, we can see its max value ending up in the middle of the grid and is lower than *hish*:

|     | V   | I   | S   | T   | A   |
| --- | --- | --- | --- | --- | --- |
| F   | 0   | 0   | 0   | 0   | 0   |
| I   | 0   | 1   | 0   | 0   | 0   |
| S   | 0   | 0   | 2   | 0   | 0   |
| H   | 0   | 0   | 0   | 0   | 0   |

### Longest common subsequence

What if the search was *fosh*? Did the user mean *fish* or *fort*? Again, using the grids, we can compare the strings. In this case, though, the longest common subsequence will be the determining factor:

|     | F   | O   | S   | H   |
| --- | --- | --- | --- | --- |
| F   | 1   | 0   | 0   | 0   |
| O   | 0   | 2   | 0   | 0   |
| R   | 0   | 0   | 0   | 0   |
| T   | 0   | 0   | 0   | 0   |

|     | F   | O   | S   | H   |
| --- | --- | --- | --- | --- |
| F   | 1   | 0   | 0   | 0   |
| I   | 0   | 0   | 0   | 0   |
| S   | 0   | 0   | 1   | 0   |
| H   | 0   | 0   | 0   | 2   |

Grid for common subsequence:

|     | F   | O   | S   | H   |
| --- | --- | --- | --- | --- |
| F   | 1   | 1   | 1   | 1   |
| I   | 1   | 1   | 1   | 1   |
| S   | 1   | 1   | 2   | 2   |
| H   | 1   | 1   | 2   | 3   |

How this was calculated was by doing the follow steps for each cell/subproblem:
- If it matches, get the top-left cell and add 1
- If it *doesn't* match, choose the greater of the 2 values above or to the left of the cell

### Exercise

- 9.3: Draw and fill in the grid to calculate the longest common substring between blue and clues.
	- The longest common substring between *blue* and *clues* is 3

|     | C   | L   | U   | E   | S   |
| --- | --- | --- | --- | --- | --- |
| B   | 0   | 0   | 0   | 0   | 0   |
| L   | 0   | 1   | 0   | 0   | 0   |
| U   | 0   | 0   | 2   | 0   | 0   |
| E   | 0   | 0   | 0   | 3   | 0   |
