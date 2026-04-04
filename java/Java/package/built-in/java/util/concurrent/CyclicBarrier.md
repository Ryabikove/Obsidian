Build-in class, which is used to manage execution in several threads. Usually is used with [[Study/1 java core/8 Threads|multithreading]].

Initialization:
```
CyclicBarrier barrier = new CyclicBarrier(int count, Supplier sup);
```

Provide methods:
- await() - stop threads, where it uses and wait until `count` equals method calls count

==After calls of await() rich count, it resets==

Example:
```
CyclicBarrier barrier = new CyclicBarrier(count, () -> {...});  
ExecutorService executor = Executors.newFixedThreadPool(count);  

for (int i = 1; i <= playersNeeded; i++) {  
	executor.submit(() -> {  
       try {  
        // Everyone calls await(). The thread stops here.  
        barrier.await();  
       } catch (Exception e) {  
          e.printStackTrace();  
       }  
    });  
}  
  
executor.shutdown();
```
