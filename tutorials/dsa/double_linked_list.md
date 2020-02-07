# Doubly Linked List
We add a pointer to the previous node in a doubly-linked list. Thus, we can go in either direction: forward or backward.

![](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/linkedlist/li2.png)


**Implementation of Doubly Linked List :**
```
# Node of a doubly linked list 
class Node: 
	def __init__(self, next=None, prev=None, data=None): 
		self.next = next # reference to next node in DLL 
		self.prev = prev # reference to previous node in DLL 
		self.data = data 
```
