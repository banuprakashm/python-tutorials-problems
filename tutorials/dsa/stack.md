# Stack

A stack is a linear data structure that stores items in a Last-In/First-Out (LIFO) or First-In/Last-Out (FILO) manner. In stack, a new element is added at one end and an element is removed from that end only.

![](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/stack/s1.png)

Think about the things you can do with such a pile of plates

* Put a new plate on top
* Remove the top plate

If you want the plate at the bottom, you have to first remove all the plates on top. Such kind of arrangement is called **Last In First Out** - the last item that was placed is the first item to go out.

Mode          | Description
------------- | -------------
empty()           | Returns whether the stack is empty
size()          | Returns the size of the stack 
top()          | Returns a reference to the top most element of the stack 
push(g)           | Adds the element ‘g’ at the top of the stack
pop()          | Deletes the top most element of the stack

-------------------------------------------------------------------------------

In the below image, although item 2 was kept last, it was removed first - so it follows the Last In **First Out(LIFO) principle.**

![](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/stack/s2.png)

## Implementation of stack :

Python’s buil-in data structure **list** can be used as a stack. Instead of push(), **append()** is used to add elements to the top of stack while **pop()** removes the element in LIFO order.

```
# Python program to demonstrate stack implementation  using list 
stack = [] 
# append() function to push element in the stack 
stack.append('a') 
stack.append('b') 
stack.append('c') 

print('Initial stack') 
print(stack) 

# pop() fucntion to pop element from stack in  LIFO order 
print('\nElements poped from stack:') 
print(stack.pop()) 
print(stack.pop()) 
print(stack.pop()) 

print('\nStack after elements are poped:') 
print(stack) 

# uncommenting print(stack.pop()) will cause an IndexError as the stack is now empty 
```
