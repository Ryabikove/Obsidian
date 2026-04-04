Built-in class, which is used to limit parallel executions.

Initialization:
```
Semaphore semaphore = new Semaphore(int permit);
```

Provide methods:
- acquire() - thread asks semaphore if permit more than 0, if yes decreace it by 1 and continue execution if not stops and wait until it will
- release() - increase permit by 1 (can not increase permit more than it was originally)

Example:
```
Semaphore semaphore = new Semaphore(2);  
ExecutorService executor = Executors.newFixedThreadPool(5);  

for (String name : employees) {  
    executor.submit(() -> {  
       try {
          // 1. Try to get a permit  
          semaphore.acquire();
       } catch (InterruptedException e) {  
          Thread.currentThread().interrupt();  
       } finally {  
          // 2. ALWAYS release in a finally block!  
          semaphore.release();  
       }  
    });  
}
```
