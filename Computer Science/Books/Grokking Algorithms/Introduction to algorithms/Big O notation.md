## Explanation

Big O notation is about representing the amount of steps/operations it takes for an algorithm to complete a task in its **worst case scenario**, like how linear/simple search takes O(n) because its worst case is 1:1 with the amount of elements given; On the other hand, binary search takes O(log n) as its worst case can only ever be as high as the log of elements.
### Algorithm running times grow at different rates

If checking an element takes 1ms and there's a billion elements, how long does it take for both search algorithms?

Simple: 1 billion milliseconds cause O(n), 1 billion elements will directly translate to 1 billion steps

Binary: 30 milliseconds cause O(log n)

### Visualizing different Big O run times

Drawing 16 boxes on a piece of paper can be done one box at a time but is O(n) as it's a whole step per box.

Folding a paper in half 4 times to make 16 boxes is O(log n) cause it's only 4 steps to make 16 boxes, $\log_{2}(16) = 4$

### Traveling Salesperson

An algorithm that has no true perfect algorithm (*yet*) with the only 100% accurate solution being O(n!)
## Exercises

1. You have a name, and you want to fnd the person’s phone number in the phone book.

O(log n) because the names are sorted and therefore can be iterated with binary search

2. You have a phone number, and you want to fnd the person’s name in the phone book.

O(n) the phone numbers are not sorted so you have to search through every individual number

3. You want to read the numbers of every person in the phone book.

O(n)

4. You want to read the numbers of just the As.

O(n / something?)