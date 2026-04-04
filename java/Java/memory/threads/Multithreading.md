Process - isolated block of operations, wich executes something.
Thread - action which is inside of process shares data and resources with other threads.

Threads can be created by hands with [[Java/package/built-in/java/lang/Thread|Thread]](depricated) or [[Java/package/built-in/java/util/concurrent/ExecutorService|ExecutorService]].

The weakest parts of data when we use multithreading is:
- Atomicity - many operations have several steps, so if several threads take one data in one time, result would be unpredictable;
- Visibility - threads have private cache, if one thread change data, another doesn't see it;
- Ordering - CPU can change the order of commands to make it more optimized, if think that commands are independent;

To make things easier there are few tools:
- [[Java/memory/threads/Syncronized|Syncronized]] - key-word, which protect data for one thread from others;
- [[Java/memory/threads/Volatile|Volatile]] -keyword, which allow write data only in main memory, not CPU cache;
- [[Java/memory/threads/AtomicClasses|AtomicClasses]] - type of classes, wich have methods that are invisible and thread-safe without using explicit synchronization. This methods guaranteed to complete as a single, uninterruptible unti of execution. (more simple than syncronized)
- [[Java/package/built-in/java/util/concurrent/lock/ReentantLock|ReentantLock]] - class provides syncronisation mechanism like [[Java/memory/threads/Syncronized|Syncronized]], but with additional features

In Java there is a tool - [[Java/package/built-in/java/util/concurrent/CountDownLatch|CountDownLatch]], which can be used in multithreading to wait until all threads send signal to this tool. How does it work:
- There is the `count` field - integer which is received when tool initializes;
- Threads call method `countDown()` - method decreaces count by 1 each time it is called;
- In one thread, where CountDownLatch has been initialized, method `await()` is called - it stops execution of this thread and wait until `count` became 0;

Also there is another tool - [[Java/package/built-in/java/util/concurrent/CyclicBarrier|CyclicBarrier]], which can be used in multithreading to stop several threads while all threads rich special point of execution.
- There is the `count` field - integer which is received when tool initializes;
- Threads call method `await()` -  it stops execution of threads where it have been called and wait;
- When all methods call `await()`, execution countinuous;


[[Java/package/built-in/java/util/concurrent/Semaphore|Semaphore]] is third main tool which allows us manage how many threads can complete at one time.
- Semaphore has `permit` quantity - number wich determinates how many threads can be parralel at one time.
- There is `acquire()` method wich threads use to take a place in queue. 
- When thread finishes it calls `release()` which frees up space in queue.