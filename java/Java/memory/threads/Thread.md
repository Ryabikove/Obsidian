Process which executes in programm.

Can be created one by hands whith class [[Java/package/built-in/java/lang/Thread|Thread]]:
```
Thread thread = new Thread(() -> method());
thread.start(); //die after execution
```
or can be created in [[Java/memory/threads/Multithreading|Multithreading]] with [[Java/package/built-in/java/util/concurrent/ExecutorService|ExecutorService]]

Characteristics:
- can't return anything but void;