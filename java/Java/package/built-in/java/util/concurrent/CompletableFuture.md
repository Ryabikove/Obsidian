Built-in class wich allows us to make [[Java/memory/async/Asyncronous pipelines|asyncronous pipelines]].

Implements by [[Future]] and [[CompletionStage]] interfaces.

Initialization - not required:
```
CompletableFuture<String> nameTask = CompletableFuture.supplyAsync(() -> { simulateDelay(1500); return "Alex"; });
```

Provide methods:
- supplyAsync(Supplier sup) - start async thread
- thenApply(Function func) - transform value
- thanAccept(Consumer sonc) - end of async thread
- thenCompose(Function func) - chain two tasks together (not asyncs)
- thanCombine(Other, BiFunc) - combine result from two async tasks

Example:
```
CompletableFuture<Double> number = CompletableFuture.supplyAsync(() -> 123.4).thenApply(Math::sqrt);  

CompletableFuture<Double> number2 = CompletableFuture.supplyAsync(() -> 2034).thenApply(Math::log);  

CompletableFuture<String> string = number2.thenCombine(number, (left, right) -> "Hello " + left + ", " + right + ";"  );  
string.thenAccept(System.out::println);
```