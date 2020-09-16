# Stacks & Queues

## Stacks

* Stack is a linear data structure, consists of Nodes. Each Node references the next Node, but does not refer to previous node.
* Stack follows a particular order in which the operations are performed. The order may be LIFO(Last In First Out) or FILO(First In Last Out).
* **Common terminology for a stack is:**

 1. **Push**: to add node.
 2. **Pop**: remove node || if empty return exception.
 3. **Top**: top of the stack.
 4. **Peek**: used to view the top || if empty return exception.
 5. **IsEmpty**: returns true when stack is empty otherwise returns false.

* When you **push** something to the stack, it becomes the new **top**.
* **Pop** remove Node from the **top**.
* The Big O for bush is O(1), it takes the same amount of time no matter how many Nodes (n)
* When we try to use **pop** we should check before if the stack empty or not with **isEmpty**.
* **Peek** can just check for the **top** node.
* With **peek** we need also to check if stack **isEmpty** to avoid the exception.

## Queue

* Its also a particular order in which the operations are performed. The order may be LIFO(Last In First Out) or FILO(First In Last Out.
* **Common terminology for a queue is:**

 1. **Enqueue**: Nodes or items that are added to the queue.
 2. **Dequeue**: Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
 3. **Front**: This is the front/first Node of the queue.
 4. **Rear**: This is the rear/last Node of the queue.
 5. **Peek**: When you peek you will view the **value** of the front Node in the queue. If called when the queue is empty an **exception** will be raised.
 6. **IsEmpty**: returns true when queue is empty otherwise returns false.

## stack vs queue visualizastion

![stack vs queue](https://techdifferences.net/wp-content/uploads/2019/06/Difference-Between-Stack-and-Queue.png)
