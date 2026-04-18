Memory area in java where java stores:
- [[Java/package/built-in/java/lang/Object/Object|Objects]];
- [[Java/variables/attributes/value/Array|Arrays]].

Heap memory shared across [[Java/memory/threads/Thread|threads]] and managed by the [[Java/memory/memory allocations/Garbage collector|garbage collector]].

Has more space than [[Java/memory/memory allocations/Stack|stack]], but slower.

It has 2 limits:
- by quantity of objects;
- by stored data volume.
When one of limits is reached, java throws [[Java/package/built-in/java/lang/OutOfMemoryError|OutOfMemoryError]].
