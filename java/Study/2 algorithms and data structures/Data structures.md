Data structures are the way we organize and store data in a computer.

There are few main types of physically stored data: 
- [[Java/variables/атрибуты переменных/значения переменной/Array|Array]] - a collection of items which stored in contiguous memory location. Fast but limited.
- [[Java/package/built-in/java/util/LinkedList|LinkedList]] consists of "nodes". Each node contains two things: the actual data and a "pointer" (reference) to the next node in the sequence. Slower than array but with dynamic size.
- [[Java/package/built-in/java/util/ArrayList|ArrayList]] has inside an simple array, but manage to contain indefinite number of elements. Faster than linked list, has dynamic size, but manipulating with data like in linked list.
- [[Java/package/built-in/java/util/HashMap|HashMap]] - collection that has unordered structure of key:value pares of data inside. Unordered, takes more space, manipulations is almost as fast as in array, has dynamic size.
See [[Java/memory/data structures/Physical stores|physical stores]] for more information.

Also there are few types of data structures which determinate how data accessed:
- *The [[Java/package/built-in/java/util/Stack|Stack]] (LIFO)* - (Last-in, First-out) means that the data has been put into structure last, would be taken from it the first.
- *The [[Java/package/built-in/java/util/Queue|Queue]] (FIFO)* - (First-in, First-out) means that the data has been put into structure firtst, would be taken from it also the first.
See [[Java/memory/data structures/Restricted data structures|Restricted data structures]] for more information

Structures can be linear like array, list etc or non-linear like:
- *The Tree* - hierarchical structure with root (top), branches (links) and leaves (data).
- *The Graph* - web relations type. There is no top or bottom, only nodes - the entities, edges - relationships, and edge type - directed or undirected.
See [[Java/memory/data structures/Non-linear data structures|Non-linear data structures]] for more information.