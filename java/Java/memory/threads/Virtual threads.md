Before Java 21, threads was wrapped around an OS thread which are expensive (take about 1MB of memory and slow to create).

Now threads are units of concurrency, managed by [[jvm]], not OS.
The best way to manage threads cause:
- Simplier code - no need in [[Java/package/built-in/java/util/concurrent/CompletableFuture|CompletableFuture]]
- No thread pools - pools used to be helpful when there were OS threads. Now there can be the personal thread for each task.
- Blocking is fine - sleepy or waiting threads are unmounted from CPU until they start executing.

==But== - if virtual thread enters a [[Java/memory/threads/Syncronized|syncronized]] block and then blocks on I/O, it "pins" the OS thread. To prevent this use [[Java/package/built-in/java/util/concurrent/lock/ReentantLock|ReentantLock]] instead of syncronized.