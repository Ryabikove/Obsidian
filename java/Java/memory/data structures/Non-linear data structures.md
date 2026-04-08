Data can be stored as line (there are before and after), and with more directions (up and down).

There are 2 main structures:
*The Tree* - hierarchical structure with root (top), branches (links) and leaves (data).
It is very efficient structure. If we look for special data in sorted array, we must check a lot of spots. But in Tree we can find any item way more faster. 
It has O(log N) coefficient of speed.
Has built-in realizations like [[Java/package/built-in/java/util/TreeMap|TreeMap]] and [[Java/package/built-in/java/TreeSet|TreeSet]].

*The Graph* - web relations type. There is no top or bottom, only nodes - the entities, edges - relationships, and edge type - directed or undirected.
Used for most complex problems in tech: finding the shortest route, reccomending movies etc.
Has no built-in realizations.

There are two ways of moving between nodes:
- *BFS* - Breadth-First Search - exploring current position before deeper ones
	- [[Java/package/built-in/java/util/Queue|Queue]] is usually used to keep track which nodes to visit next
	- This way is the best for finding shortest path in terms of steps 
- *DFS* - Depth-First Search - go to the deepest level and start exploring from the bottom to the top
	- [[Java/package/built-in/java/util/Stack|Stack]] or recursion are usually used to remember the way back
	- This way best for exhaustive searching or checking every possible outcome