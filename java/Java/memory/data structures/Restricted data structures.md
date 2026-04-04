There are few data structures which are about how to access data.

*The [[Java/package/built-in/java/util/Stack|Stack]] (LIFO)* - (Last-in, First-out) means that the data has been put into structure last, would be taken from it the first.
Key operations:
- push() - add an item to the top;
- pop() - remove item from the top;
- peek() - look at the item without removing it.
It is perfect for "reversing" things or keeping track of history. Browser's "Back" button and the "Undo" (Ctrl+Z) feature in ide are powered by It.

*The [[Java/package/built-in/java/util/Queue|Queue]] (FIFO)* - (First-in, First-out) means that the data has been put into structure firtst, would be taken from it also the first.
Key operations:
- add() / enqueue() - join the back of the line;
- poll() / dequeue() - leave the front of the line;
- peek() - see who is next in the line.
It is perfect for processing tasks in exact order they arrived. It is like a printer handling documents or a web server handling incoming requests.

Both structures has O(1) speed coefficient in every operation.