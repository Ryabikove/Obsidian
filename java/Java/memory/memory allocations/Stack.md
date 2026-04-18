Memory area in java where java stores:
- Method calls;
- [[Java/variables/memory allocations/Local|Local]] variables;

Each [[Java/memory/threads/Thread|thread]] has his own stack.
Has more speed than [[Java/memory/memory allocations/Heap|heap]], but less space.

It has 1 limit:
- quantity of nested method calls (recursion)
When limit is reached, java throws [[Java/package/built-in/java/lang/StackOverflowError|StackOverflowError]].