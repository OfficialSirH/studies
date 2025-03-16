[[Selection sort]]
## Linked lists

A list of connected addresses that can be scattered all over memory without a need to place elements side by side but with the downside of always being sequential.

### Pros

- Fast insertion (O(1) insertion)
- No need to move elements around when inserting more elements
- No need to shift elements when removing elements (O(1) deletion)

### Cons

- Always sequential access (O(n) reading)
## Arrays

A list of elements that are all side by side to each other in memory, which allows for random access, but with the downside of slower insertions and deletions.

### Pros

- Random Access (O(1) reading)

### Cons

- Slow deletion and insertions (O(n))
- elements always have to be side by side, which leads to a lot of element relocating if an element insert causes collision with other used memory chunks

## Selection Sort
## Exercises

- Suppose you’re building an app to keep track of your finances. Every day, you write down everything you spent money on. At the end of the month, you review your expenses and sum up how much you spent. So, you have lots of inserts and a few reads. Should you use an array or a list?

A list is the best approach as it's able to more easily insert with an O(1) and it's only read once at the end of the month to sum up all of the expenses.

- Suppose you’re building an app for restaurants to take customer orders. Your app needs to store a list of orders. Servers keep adding orders to this list, and chefs take orders of the list and make them. It’s an order queue: servers add orders to the back of the queue, and the chef takes the first order of the queue and cooks it. Would you use an array or a linked list to implement this queue?

A linked list would fit since the primary operations done for the orders are insertions and deletions, which are done at O(1) for linked lists.

- Let’s run a thought experiment. Suppose Facebook keeps a list of usernames. When someone tries to log in to Facebook, a search is done for their username. If their name is in the list of usernames, they can log in. People log in to Facebook pretty often, so there are a lot of searches through this list of usernames. Suppose Facebook uses binary search to search the list. Binary search needs random access—you need to be able to get to the middle of the list of usernames instantly. Knowing this, would you implement the list as an array or a linked list?

An array since arrays allow for random access and therefore can be read anywhere at O(1)

- People sign up for Facebook pretty ofen, too. Suppose you decided to use an array to store the list of users. What are the downsides of an array for inserts? In particular, suppose you’re using binary search to search for logins. What happens when you add new users to an array?

Arrays have an insertion time of O(n) due to the need of shifting all following elements after the inserted element. Due to the necessity of an array being sorted, inserting new elements can cause issues for binary search.

- In reality, Facebook uses neither an array nor a linked list to store user information. Let’s consider a hybrid data structure: an array of linked lists. You have an array with 26 slots. Each slot points to a linked list. For example, the first slot in the array points to a linked list containing all the usernames starting with a. The second slot points to a linked list containing all the usernames starting with b, and so on. Suppose Adit B signs up for Facebook, and you want to add them to the list. You go to slot 1 in the array, go to the linked list for slot 1, and add Adit B at the end. Now, suppose you want to search for Zakhir H. You go to slot 26, which points to a linked list of all the Z names. Ten you search through that list to fnd Zakhir H. Compare this hybrid data structure to arrays and linked lists. Is it slower or faster than each for searching and inserting? You don’t have to give Big O run times, just whether the new data structure would be faster or slower.

It's faster cause it has O(1) for finding the specific letter category and O(1) for the insertion into those categories.