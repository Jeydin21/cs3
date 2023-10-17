Name: Jeydin Pham

Date: 10/17/2023

Period: 5

# Unit 5: Stacks

## Introduction to Stacks in Java

### What is a stack?

- A stack is a data structure that follows the Last-In, First-Out (LIFO) principle. In simpler terms, the last item you put in is the first one to come out. It's like a stack of plates; you add a plate to the top of the stack and also remove from the top.

## Basic Operations

- push() - Add an item to the top of the stack
- pop() - Remove an item from the top of the stack
- peek() - Look at the top item of the stack
- top() - Get the top item of the stack
- isEmpty() - Check if the stack is empty

## Importing the Stack Class

```java
import java.util.Stack;
```

## Initializing a Stack

```java
Stack<Integer> stack = new Stack<>();
```

## Push Operation

```java
stack.push(10);
stack.push(20);
stack.push(30);
```

## Pop Operation

```java
int topElement = stack.pop(); // Removes and returns top element (in this case it would be the 30 just added)
```

## Peek Operation

```java
int topElement = stack.peek(); // Returns the top element (in this case it would be 20)
```

## Empty Operation

```java
boolean isEmpty = stack.isEmpty(); // Returns true if the stack is empty, false otherwise
```

## TIPS/REMINDERS

# Example

```java
import java.util.Stack;
import java.util.Scanner;

public class ParanthesisChecker {
    public static void main(String[] args) {
        // Create a stack to store paranthesis
        Stack<Character> stack = new Stack<Character>();

        // Create a scanner to read input from the user
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter an expression
        System.out.print("Enter an expression: ");
        String expression = scanner.nextLine();

        // Iterate through each character in the expression
        for(char ch: expression.toCharArray()) {
            if(ch == "(" || ch == "[" || ch == "{") {
                // If the character is an opening paranthesis, push it onto the stack
                stack.push(ch);
            } else {
                if(ch == ")" || ch == "]" || ch == "}") {
                // If the character is a closing paranthesis, check if it matches the top of the stack
                    if(stack.isEmpty()) {
                        // If the stack is empty, the expression is not balanced
                        System.out.println("The expression is not balanced.");
                        return;
                    }
    }
}
```
