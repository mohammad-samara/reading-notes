# Linked List


## Definition

Linked Lists are like arrays but they dont have index, instead they are connected to each other in sequence, they are called nodes.

There are two types of links, singly which means a node is linked to the next node only, while double means its linked to more than one node.

## Parts of a linked list:
- head 
- nodes
- null value 

## Parts of a single node:
- data
- reference to the next node 

## types of a linked lists:
- Singly linked lists
- doubly linked list
- circular linked list

## Traversal

* You can't use forEach or for loop, we must use next and with a while loop which will prevent looking into a null node.

* We start at the head node by setting the Current to Head (current is the referenec type of type).

* We need if statement to determine when to break the loop by giving a return statement when that condition is met.

Because of the condition that `while Current is not NULL` we wont run into a problem of getting `NullReferenceException`

* We know we are at the end of the loop when Current reaches null and that makes the while loop breaks

* Big O of time for includes is O(n) which is linear, because at its worst case, the node we want is the last one.

* Big O of space for includes would be O(1) because there is no additional space being used than what is already given to us.

## Adding a note with O(1)

* You must make sure every reference to each node is properly assigned.

* To add with o(1) efficiency, the new node must replace the head.

* We can do that by: 
1- Set Current = Head

2- Start the new node and pass them into `Add()`

3- Change `newNode.Next` from null to `Head`, and that would be `Node1`

4- We need to reassign where the head points at and current aswell

## Adding a note with O (n)

1- if you want to add to the middle (6 for example) we must assign a new node and give it a value.

2- We can do `AddBefore` or `AddAfter` 

3- If we want to add node6 in place of node4, we need to set current to node3

4- we can set node6.Next to node4, but that means node3 and node6 are pointing at node4

5- Change node3.Next to node6

* Big(O) in this depends on where we want to add our node, worst is at the last node

## Printing out Nodes

* We need to leverage our Current node and a while loop to traverse, when the condition is met, while loop breaks and we print out the node.

