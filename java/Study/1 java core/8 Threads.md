Process - isolated block of operations, wich executes something.
Thread - action which is inside of process shares data and resources with other threads.

*Multithreading*
Threads can be created by hands with [[Java/package/built-in/java/lang/Thread|Thread]](depricated) or [[Java/package/built-in/java/util/concurrent/ExecutorService|ExecutorService]].

The weakest parts of data when we use multithreading is:
- Atomicity - many operations have several steps, so if several threads take one data in one time, result would be unpredictable;
- Visibility - threads have private cache, if one thread change data, another doesn't see it;
- Ordering - CPU can change the order of commands to make it more optimized, if think that commands are independent;

To make things easier there are few tools:
- [[Java/memory/threads/Syncronized|Syncronized]]
- [[Java/memory/threads/Volatile|Volatile]]
- [[Java/memory/threads/AtomicClasses|AtomicClasses]]
- [[Java/package/built-in/java/util/concurrent/lock/ReentantLock|ReentantLock]]

In Java there is a tool - [[Java/package/built-in/java/util/concurrent/CountDownLatch|CountDownLatch]], which can be used in multithreading to wait until all threads send signal to this tool.

Also there is another tool - [[Java/package/built-in/java/util/concurrent/CyclicBarrier|CyclicBarrier]], which can be used in multithreading to stop several threads while all threads rich special point of execution.

[[Java/package/built-in/java/util/concurrent/Semaphore|Semaphore]] is third main tool which allows us manage how many threads can complete at one time.

For more information see [[Java/memory/threads/Multithreading|multithreading]].

*Asyncronous*
Asynchronous tasks means that task executed not parralel at all, but without ordering.
While one task is waiting result, another can execute. Process time always uses for execution and never for wait.

For more information see [[Java/memory/async/Asyncronous pipelines|asyncronous pipelines]].
The main tool for asyncronous is [[Java/package/built-in/java/util/concurrent/CompletableFuture|CompletableFuture]]. It allows us to build asyncronous pipelines.

*Virtual threads*
Appears only in Java 21+
The best way to manage threads cause:
- Simplier code
- No thread pools
- Blocking is fine

==But== - if virtual thread enters a [[Java/memory/threads/Syncronized|syncronized]] block and then blocks on I/O, it "pins" the OS thread. To prevent this use [[Java/package/built-in/java/util/concurrent/lock/ReentantLock|ReentantLock]] instead of syncronized.

For more see [[Java/memory/threads/Virtual threads|Virtual threads]]