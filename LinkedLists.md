# Unit 7 Notes: Linked Lists
A linked list is a data structure consisting of nodes where each node contains data and a reference to the next node in the sequence.

To go through a linked list, you start at the head (first node) and follow the references from one node to the next until you reach the end (a node that points to null).


Creating and Printing Lists
Understand how to construct a linked list and print its elements.

To construct a linked list, you start by creating the first node (often referred to as the head). Each subsequent node is linked as the next node of the previous one.
To print elements of a linked list, you'll need to iterate through the list using a loop.

See Ex. 1

Counting Specific Elements
Understand how to count elements that meet a certain condition, like counting odd numbers:
See Ex. 2

Creating a NodeList
To start a list:

```java
ListNode head = new ListNode("Data", null);  // A single node with data and no next node
```

To add nodes:

```java
head = new ListNode("NewData", head);  // Adds a new node before the current head
```

Adding a Node at the Front
```java
ListNode newNode = new ListNode("Data", head);
head = newNode;
```

Adding A Node at the end
```java
ListNode current = head;
while (current.getNext() != null) {
		current = current.getNext();
}
current.setNext(new ListNode("Data", null));
```

Removing a Node
To remove a node, you must adjust the next reference of the preceding node to skip the node to be deleted.

Finding a Node
To find a node with a specific value:
```java
ListNode current = head;
while (current != null && !current.getValue().equals("ValueToFind")) {
		current = current.getNext();
}// If current is not null, the node was found
```
Empty List
Always check if the list is empty (head == null) before performing operations.

Single-Element List
Ensure that operations work when there is only one element (head.getNext() == null).

End of List
When iterating, the end is reached when current.getNext() == null.

Common Patterns
Traversing the List
```java
ListNode current = head;
while (current != null) {
		// Process current node's value
		current = current.getNext();
}
```

Printing the List
```java
ListNode current = head;
while (current != null) {
		System.out.println(current.getValue());
		current = current.getNext();
}
```
Reversing the List
```java
ListNode prev = null;
ListNode current = head;
ListNode next = null;
while (current != null) {
		next = current.getNext();
		current.setNext(prev);
		prev = current;
		current = next;
}
head = prev;

```
Counting Specific Elements
Counting Nodes
```java
int count = 0;
ListNode current = head;
while (current != null) {
		count++;
		current = current.getNext();
}
return count;
```
