# Queue

A queue is a useful data structure in programming. It is similar to the ticket queue outside a cinema hall, where the first person entering the queue is the first person who gets the ticket. Queue follows the **First In First Out(FIFO)** rule - the item that goes in first is the item that comes out first too.

![](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/queue/q1.png)

**Implementation using list :** List is a Python’s built-in data structure that can be used as a queue. Instead of enqueue() and dequeue(), append() and pop() function is used.

```
# Python program to demonstrate queue implementation using list 

# Initializing a queue 
queue = [] 

# Adding elements to the queue 
queue.append('a') 
queue.append('b') 
queue.append('c') 

print("Initial queue") 
print(queue) 

# Removing elements from the queue 
print("\nElements dequeued from queue") 
print(queue.pop(0)) 
print(queue.pop(0)) 
print(queue.pop(0)) 

print("\nQueue after removing elements") 
print(queue) 

# Uncommenting print(queue.pop(0)) will raise and IndexError as the queue is now empty 
```
**Implementation using collections.deque :** Queue in Python can be implemented using **deque** class from the collections module. Instead of enqueue and deque, append() and popleft() functions are used.

```
# Python program to demonstrate queue implementation using collections.dequeue 
from collections import deque 

# Initializing a queue 
q = deque() 

# Adding elements to a queue 
q.append('a') 
q.append('b') 
q.append('c') 

print("Initial queue") 
print(q) 

# Removing elements from a queue 
print("\nElements dequeued from the queue") 
print(q.popleft()) 
print(q.popleft()) 
print(q.popleft()) 

print("\nQueue after removing elements") 
print(q) 

# Uncommenting q.popleft() will raise an IndexError as queue is now empty 

```
**Implementation using queue.Queue:** Queue is built-in module of Python which is used to implement a queue. queue.Queue(maxsize) initializes a variable to a maximum size of maxsize. A maxsize of zero ‘0’ means a infinite queue. This Queue follows FIFO rule.

```
# Python program to 
# demonstrate implementation of wqqueue using queue module 
from queue import Queue 
# Initializing a queue 
q = Queue(maxsize = 3) 
# qsize() give the maxsize of the Queue 
print(q.qsize()) 
# Adding of element to queue 
q.put('a') 
q.put('b') 
q.put('c') 

# Return Boolean for Full Queue 
print("\nFull: ", q.full()) 

# Removing element from queue 
print("\nElements dequeued from the queue") 
print(q.get()) 
print(q.get()) 
print(q.get()) 

# Return Boolean for Empty Queue 
print("\nEmpty: ", q.empty()) 

q.put(1) 
print("\nEmpty: ", q.empty()) 
print("Full: ", q.full()) 

# This would result into Infinite Loop as the Queue is empty. print(q.get()) 
```
  
