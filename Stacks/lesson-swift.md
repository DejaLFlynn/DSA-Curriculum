# Stacks

## Goals
- Understand what's a Stack
- LIFO
- Stack Methods
- Understand how to implement a stack

## Lesson 

## What's a Stack?

Stacks are very common. Here are some common examples of things you would stack in real life:

- Dishes
- Pancakes 
- Books
- Dollar Bills

Just like the way you represent stacks in the physical world, we do the same in computer science.

![Stack of Dishes](assets/stack-dishes.jpeg)

There are two fundemental concepts with a stack collection:

1. When you add a new element it goes on top of the stack.
2. When you remove an element you're only allowed to remove the one on top.

This is a very famous concept called LIFO.

## LIFO

![Stack of Dishes](assets/stack-graphic.png)

LIFO stands for 'Last In First Out'. 

In stacks only two operations are allowed: push the item into the stack, and pop the item out of the stack. A stack is a limited access data structure; elements can only be added and removed from the stack only at the top. 

Just like in the physical world, if you tried to pull out a dish from the middle it would all come crashing.

## Stack Use Cases

Here are some real world applications of stacks:

- Back & Forward button on Web Browsers.
- Reversing a word. You push a word letter by letter, then pop letters from the stack.
- Undo mechanism. Example, undo in a text editor.
- Syntax checking for compilers. Example, checking for parentheses and braces.
- Memory allocation uses stacks at the architectural level. Memory for local variables is also managed using a stack.

## Stack Methods

1. **push(value) :** Add new element to the top of the stack.
2. **pop() :** Remove element from top of the stack and return it. 
3. **peek() :** Returns the top element of the stack without removing it.
4. **isEmpty() :** Returns a boolean indicating if the stack is empty or not.

## Stack Implementation

There are two ways of implementing Stacks. One is the hard traditional way and the other is the easier way using Arrays. They both fundementally tackle the same problems, so for this lesson we will follow the Array route. 

### Container Class

```swift
class Stack<T> {

  private var arr: [T] = []

  public init() {}

}
```

This is pretty straight forward. We don't want to initialize a stack with any value. The only important member property of the class is an Array to hold our elements.

### push(value)

What do we want to accomplish? Adding a new element to the END of the stack. 

```swift
func push(_ newElement: T) {
  arr.append(newElement)
}
```

### pop()

Now we want to remove and return the last element, which is also very simple using Arrays.

```swift
func pop() -> T? {
  return arr.removeLast()
}
```

### peek()

We want to just be able to access the element on top of the stack. 

```swift
func peek() -> T? {
  return arr.last
}
```

### isEmpty()

Check if the stack is empty.

```swift
func isEmpty() -> Bool {
  return arr.count == 0
}
```

### Putting it all Together

```javascript
class Stack<T> {

  private var arr: [T] = []

  public init() {}

  func push(_ newElement: T) {
    arr.append(newElement)
  }

  func pop() -> T? {
    return arr.removeLast()
  }

  func peek() -> T? {
    return arr.last
  }

  func isEmpty() -> Bool {
    return arr.count == 0
  }
}
```

As you can see, pretty simple right? Stacks are simple to conceptualize and code once you understand the fundementals. 

## Excersize

Implement a Stack in the traditional way using Linked Lists. You may not use any Array or built in Array methods. 

Implement the linked list based stack with the following methods:

1. **push(value) :** Add new element to the top of the stack.
2. **pop() :** Remove element from top of the stack and return it. 
3. **peek() :** Returns the top element of the stack without removing it.
4. **isEmpty() :** Returns a boolean indicating if the stack is empty or not.
