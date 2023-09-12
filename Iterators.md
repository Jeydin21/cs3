Name: Jeydin Pham

Date: 9/11/2023

Period: 5

# Unit 1 Notes: Iterators

### Intro to Iterators

- Iterators are **objects**
  - These objects are used to **traverse** through collections
  - Collections are lists, sets, maps, etc...
  - Iterators provide methods to access and manupulate elements within the collection

### Creating an Iterator

**You need a collection first**

**Then you can create an iterator**

```java
List<Integer> nums = new ArrayList<>();
Iterator<Integer> iterator = nums.iterator();
```

## Iterator Methods

### .next()

- It allows you to move to the next element in the collection and retrieve its value
- It also moves the iterator's position forward

```java
while(iterator.hasNext(1) {
    Integer number = iterator.next();
})
```

### .hasNext()

- Boolean functions returning to determine if there is a next element
- Commonly used as a while loop condition

### .remove()

- It removes the current element
  - **Be careful with remove especially within a for each loop**

## ListIterator Interface

- ListIterator is an offshoot of Iterator made specifically for lists
- Allows us to move both directions

### .previous()

- Only available with ListIterator, you can move <u>backward</u> in the list using the previous() method

### .set()

- The set() method allows you to update the current element's value

```java
ListIterator.set(newValue); // Sets current element to "newValue"
```

### .add()

- It lets you <u>insert</u> a new element at the current position
  - **Be careful when editing any list/collection with Iterators**
- Modification is always applied to the last, next, or previous call when using the iterator

#

| <u>this</u> | is  | us  |
| ----------- | --- | --- |

```java
.next();
```

| this | <u>is</u> | us  |
| ---- | --------- | --- |

```java
.set("###");
```

| this | ### | us  |
| ---- | --- | --- |
