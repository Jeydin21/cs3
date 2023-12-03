# Unit 3 Notes: Sets

## What is a Set?

- In Java, a set is a collection that does not allow duplicate elements
- Sets are part of Java Collection Framework and are used to store unique elements

## Set Interface

- A set is defined as an interface in Java
- To use a set, we need to instantiate a concrete class that implements this interface
- Two common implementations are **Hash Sets** and **Tree Sets**

## Hash Set

- Hash Set is an implementation of a set that uses a hash table for storage
- A hash tabe is a data structure that allows for efficient insertion, deletion, and retrieval of <u>elements</u>
- Hash Set does not <u>guarantee</u> any specific order of elements

```java
Set<String> hashbrown = new HashSet<>
```

## Tree Set

- Tree Set is another implementation but it uses binary
- Elements are <u>sorted</u>
- Tree Set is slower, but always <u>maintains</u> a <u>sorted</u> order

```java
Set<Integer> cypress = new TreeSet<>;
```

## Common Set Operations

- Adding elements

```java
hashbrown.add("apple");
cypress.add(42);
```

- Removing elements

```java
hasbrown.remove("apple");
cypress.remove(42);
```

- Clearing the Set (removes all)

```java
hashbrown.clear();
cypress.clear();
```

- Getting the size

```java
int size = hashbrown.size();
int tsize = cypress.size();
```

## Set Notation (operations on sets)

- Union on SetA and SetB

```java
setA.addAll(setB); // Union of setA.setB
```

- Intersection
  - Intersection of two sets contains element that are common to both sets

```java
Set<Integer> int = new HashSet<>(setA);
int.retainAll(setB);
```

- Difference
  - The difference between sets contains elements that are in one set but not the other

```java
Set<Integer> diff = new HashSet<>(setA);
diff.removeAll(setB);
```

## HashSet vs TreeSet

- HashSet is chosen when:
  - You need faster processing
  - Order of elements doesn't matter
  - You want to avoid duplicates
- TreeSet is chosen when:
  - You need elements to be sorted
  - You don't mind slower processing
  - You want a naturally sorted list
