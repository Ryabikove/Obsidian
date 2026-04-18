Mechanism which removes unused [[Java/memory/Object|objects]].

There are 4 main types of GC:
- Serial;
- Parallel;
- G1 (default in modern java):
	- Splits [[Java/memory/memory allocations/Heap|heap]] into regions;
	- Collects in small chunks;
	- Has predictable pause times.
- ZGC:
	- Has ultra short pauses (few ms);
	- Mostly concurrent;
	- Handles huge heaps (TB scale).
==While GC is cleaning memory, all threads are paused==


GC deletes objects from memory if they aren't reachable.
To detect which variable isn't reachable, GC uses reachability analysis:
1. [[Java/variables/memory allocations/Local|Local variables in stack]];
2. Active [[Java/memory/threads/Thread|threads]];
3. [[Java/variables/memory allocations/Static|Static variables]];
4. [[Java/tools/JNI|JNI references]];
```
Person p = new Person(); // p link in stack; Object in heap. So object is reachable
p = null; // No reference in stack; Object isn't reachable
```

When analysis is end:
1. Mark all reachable objects;
2. Remove all unmarked objects;
3. Move all marked together;
4. Compact memory.

Because of most objects usefull for a short time after creation, GC splits memory in heap on 2 peaces:
1. Young generation:
	- New objects created here;
	- Fast, GC executes frequently
	- Has parts:
		- Eden;
		- Survivor spaces (S0, S1);
2. Old generation:
	- Long lived objects here;
	- GC executes less often (slower, heavier)

Flow of objects :
1. Object created -> Eden;
2. Survives GC -> moves to Survivor;
3. Survive multiple cycles -> moved to Old Gen;

You can call a running GC manually with `System.gc()`, but it cannot guarantee, that it will actually run GC immediately.