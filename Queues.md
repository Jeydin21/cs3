Name: Jeydin Pham

Date: 10/19/2023

Period: 5

# Introduction to Queues in Java for Beginners

## What is a Queue?

A queue is a data structure that follows the First-In, First-Out (FIFO) principle. The first element to be added is the first one to be removed, much like a real-life queue or line.

## Basic Operations

- **Enqueue**: Adding an element to the rear of the queue.
- **Dequeue**: Removing the front element from the queue.
- **Front/Peek**: Accessing the front element without removing it.
- **isEmpty**: Checking if the queue is empty.
- **Size**: Getting the number of elements in the queue.

## How to Use Queues in Java

### Importing the Queue Interface

Java's Queue is an interface, so you'll need to use a class that implements it, like `LinkedList` or `ArrayDeque`:

```java
import java.util.LinkedList;
import java.util.Queue;
```

### Initializing a Queue

To initialize a queue, you can do the following:

```java
Queue<Integer> queue = new LinkedList<>();
```

### Enqueue Operation

To add an element to the rear of the queue, use the `add()` or `offer()` method:

```java
queue.add(10);
queue.offer(20); // This method is preferable as it doesn't throw an exception when the queue is full.
```

### Dequeue Operation

To remove an element from the front of the queue, use the `poll()` or `remove()` method:

```java
int frontElement = queue.poll(); // Removes and returns the front element, returns null if the queue is empty
```

### Front/Peek Operation

To access the front element without removing it, use the `peek()` or `element()` method:

```java
int frontElement = queue.peek(); // Returns the front element without removing, returns null if the queue is empty
```

### isEmpty and Size Operations

To check if the queue is empty and to get its size:

```java
boolean isEmpty = queue.isEmpty();
int size = queue.size();
```

## Important Tips and Notes

1. **Null Handling**: Methods like `poll()` and `peek()` return `null` if the queue is empty. Always check for `null` before using these values.

2. **Exception Handling**: Methods like `add()` and `remove()` throw exceptions when trying to operate on an empty queue or a full queue (in case of bounded queues). Use `offer()` and `poll()` to safely avoid exceptions.

3. **Generics**: Like stacks, queues in Java are generic and can store elements of any type:

   ```java
   Queue<String> stringQueue = new LinkedList<>();
   ```

4. **PriorityQueue**: Java also has a `PriorityQueue` class, where elements are ordered by their natural ordering or by a custom comparator.

5. **Thread Safety**: The basic Queue implementations like `LinkedList` and `ArrayDeque` are not thread-safe. Use `ConcurrentLinkedQueue` for a thread-safe option.

6. **Iteration**: You can iterate through a queue using iterators or for-each loops, but modifying the queue while iterating can produce unexpected results.

   ```java
   for (int element : queue) {
   System.out.println(element);
   }
   ```

7. **ArrayDeque for Efficiency**: For a more memory-efficient implementation, consider using `ArrayDeque`. It's also generally faster for enqueuing and dequeuing elements.

By understanding these basics, you'll be well-equipped to use queues in Java effectively. Happy coding!

# Example

```java
import java.util.LinkedList;
import java.util.Queue;

class Main {
  public static void main(String[] args) {
    // Create a Queue using LinkedList
		Queue<String> queue = new LinkedList<>();

		// add types of apples to the queue
		queue.add("Granny Smith");
		queue.add("Fuji");
		queue.add("Gala");
		queue.add("Braeburn");

		//Display the queue
		System.out.println("Queue: " + queue);

		// Remove elements from the queue
		String removedApple = queue.remove();
		System.out.println("Removed apple: " + removedApple);

		// Display updated queue of apples
		System.out.println("Updated queue: " + queue);

		// peek at the front of queue w/o removing
		String peekApple = queue.peek();
		System.out.println("Peeked apple: " + peekApple);

		// remove from queue using poll
		String pollApple = queue.poll();
		System.out.println("Removed apple using poll: " + pollApple);

		// Check if the queue is empty
		boolean isEmpty = queue.isEmpty();
		System.out.println("Is the queue Empty? " + isEmpty);

  }
}
```
