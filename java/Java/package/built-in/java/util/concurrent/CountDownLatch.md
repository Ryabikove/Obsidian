Built-in class, wich is used to manage of programm execution. Usually is used with [[Study/1 java core/8 Threads|multithreading]].

Initialization:
```
CountDownLatch latch = new CountDownLatch(int count);
```

Provide methods:
- countDown() - decreace count by 1
- await() - stop thread, where it uses and wait until count become 0

==Count cannot be reset, for loops use [[Java/package/built-in/java/util/concurrent/CyclicBarrier|CyclicBarrier]]==

Example:
```
CountDownLatch latch = new CountDownLatch(3);
ExecutorService executor = Executors.newFixedThreadPool(3);
for (int i = 0; i < 3; i++) {  
    executor.submit(() -> {  
       try {...}
       catch (InterruptedException e) { Thread.currentThread().interrupt();}
       finally {latch.countDown();}  
    });  
}  
//  The main thread blocks here until the latch count is 0  
latch.await();
```