[[Grokking Algorithms]]

## The classroom scheduling problem

| Class   | Start    | End      |
| ------- | -------- | -------- |
| Art     | 9 AM     | 10 AM    |
| English | 9:30 AM  | 10:30 AM |
| Math    | 10 AM    | 11 AM    |
| CS      | 10:30 AM | 11:30 AM |
| Music   | 11 AM    | 12 PM    |

The above schedule shows that each class overlaps the next and the goal of this schedule is to have as many classes as possible, so how is this solved? In a pretty trivial way, surprisingly, just by starting with the class that ends the soonest, Art in this case, and then choosing the next soonest class, Math for this case due to English having been overlapped by the previous class, and so on and so forth until you have Art, Math and Music, the most classes with no overlap. This is called getting the locally optimal solution at each step to end with the globally optimal solution.

## The knapsack problem

A thief with only 35 lbs. of carrying space wants to get as much money as possible within their bag, they're given the following options:
- Stereo - $3000 - 30lbs
- Laptop - $2000 - 20lbs
- Guitar - $1500 - 15lbs
With a greedy algorithm, you'd just go for the most expensive item first and continue from there, but the bag is near full just with the stereo but is *close* to the highest possible value. Although the better outcome would be getting both the laptop and the guitar to get an extra $500, the stereo gets pretty close with a very simple algorithm.

### Exercises

- 8.1: You work for a furniture company, and you have to ship furniture all over the country. You need to pack your truck with boxes. All the boxes are of different sizes, and you’re trying to maximize the space you use in each truck. How would you pick boxes to maximize space? Come up with a greedy strategy. Will that give you the optimal solution?
	- Go from biggest to smallest; simply put all of the largest boxes into the truck first and then put in smaller and smaller boxes each after the previous larger sized box. This wouldn't give the optimal solution as there's likely to be leftover small gaps between and around the larger boxes that could've been filled with the smaller boxes.
- 8.2: You’re going to Europe, and you have seven days to see everything you can. You assign a point value to each item (how much you want to see it) and estimate how long it takes. How can you maximize the point total (seeing all the things you really want to see) during your stay? Come up with a greedy strategy. Will that give you the optimal solution?
	- Go for the highest valued points first, the areas that I'd want to see the most, and then go for the lower and lower points. This might not be the optimal solution as some of the high points areas may take up more time than the combination of smaller points areas.

## The set-covering problem

| Radio Station | Available In |
| ------------- | ------------ |
| Kone          | ID, NV, UT   |
| Ktwo          | WA, ID, MT   |
| Kthree        | OR, NV, CA   |
| Kfour         | NV, UT       |
| Kfive         | CA, AZ       |
| etc..         | etc..        |
Looking at the above table for this problem, if a radio show wanted to cover all 50 states in as few radio stations as possible, they would have to list all possible subsets of all stations and then choose the set that has the smallest number of stations that covers all 50 states. The problem with this is that it becomes exponentially harder to calculate all the subsets for each new radio station that is added, leading to an O(2^n) time, because there are 2^n stations. This is where [[#Approximation algorithms]] come in to play.
### Approximation algorithms

These kinds of greedy algorithms are really simple and helpful for this kind of problem as they are done really fast and give an approximate answer that would be considered "good enough" for this situation. How it works is as follows:
1. Pick a station that covers the most states that haven't been covered yet. The station can cover some states that have already been covered.
2. Repeat until all states have been covered.

### Exercises

8.3: Quicksort - not greedy
8.4: Breadth-first search - greedy
8.5 Dijkstra's algorithm - not greedy

## NP-complete problems

An example NP-complete problem, the traveling salesman, is a problem that grows by a factorial of the amount of routes that are added to the problem and is unable to be trivially calculated after enough routes are included. Problems like these are best handled through approximation, like for the traveling salesman, a decent approximation would be to choose an arbitrary city and then going for the next closest city and so on.

### How do you tell if a problem is NP-complete?

NP-complete problems can be seen in many situations where you have to figure out what combination of things can fulfill a task the best. Some ways to see a pattern of what is NP-complete are the following:
- An algorithm that slows done exceedingly fast the more items that need to be calculated
- "All combinations of X" usually point to an NP-complete problem. 
- Do you have to calculate “every possible version” of X because you can’t break it down into smaller sub-problems? Might be NP-complete. 
- If your problem involves a sequence (such as a sequence of cities, like traveling salesperson), and it’s hard to solve, it might be NP-complete. 
- If your problem involves a set (like a set of radio stations) and it’s hard to solve, it might be NP-complete. 
- Can you restate your problem as the set-covering problem or the traveling-salesperson problem? Then your problem is definitely NP-complete.

### Exercises

- 8.6: A postman needs to deliver to 20 homes. He needs to find the shortest route that goes to all 20 homes. Is this an NP-complete problem?
	- Yes, traveling salesman problem
- 8.7: Finding the largest clique in a set of people (a clique is a set of people who all know each other). Is this an NP-complete problem?
	- Yes, set-covering problem
- 8.8: You’re making a map of the USA, and you need to color adjacent states with different colors. You have to find the minimum number of colors you need so that no two adjacent states are the same color. Is this an NP-complete problem?
- No