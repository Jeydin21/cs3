# Unit 9 Notes: Big O Notation
The processing complexity of various sorting algorithms and operations in different data structures

Big O Notation expresses an upper bound on the time complexity for an algorithm


## Big O Notation Graph
![](https://paper-attachments.dropbox.com/s_2D428973624E7FC84C7D69D11421DE762BEA6B6F3361231FCDCAE0425D14526F_1664885448372_Untitled.drawio+17.png) 

### Insertion
- Best case: O(n)
- Worst case: O($n^2$)

### Quick
- Best case: O(n log n)
- Worst case: O($n^2$)

### Bubble
- Best case: O($n^2$)

### Merge
- Best case: O(n log<sub>2</sub> n)
- Worst case: O(n log<sub>2</sub> n)

## Data Structures Operations

### Array
- Adding to front: O(n)
- Adding to middle O(n)
- Adding to end: O(1)
- Deleting item: O(n)

### Linked List
- Adding to front: O(1)
- Deleting item (known location): O(1)

### Tree Set (Balanced)
- Adding an item: O(log<sub>2</sub>n)
- Searching an item: O(log<sub>2</sub>n)
- Travsersing: O(n)

### Hash Set
- Adding an item: O(1)

### Binary Search Tree
- Adding to the tree: O(log<sub>2</sub>n)
- Searching in the tree: O(log<sub>2</sub>n)
- Travsersing in the tree: O(n)
