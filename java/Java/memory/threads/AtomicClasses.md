Bunch of classes, which have special methods, that behave like single, uninterrupltable operation.

This methods protect data from collisions in [[Study/1 java core/8 Threads|multithreading]] without using explicit synchronization.
It uses a low-level CPU instruction called CAS(Compare-And-Swap) to ensure the operation is thread-safe without the heavy overhead of a syncronized lock.

Compare-And-Swap works this way:
- Doesn't lock the thread
- Read current value
- Calculate new value
- Swap value - if value is still same, change to new; if value has already been changed, try again with new value
It's much faster than [[Java/memory/threads/Syncronized|Syncronized]]

Methods in this classes complete fully or doesn't complete at all.

There are followed atomic classes:
- [[AtomicInteger]]
- [[AtomicBoolean]]
- [[AtomicIntegerArray]]
- [[AtomicLong]]
- [[AtomicLongArray]]
- [[AtomicReference]]
- [[AtomicReferenceArray]]
- [[AtomicMarkableReference]]
- [[AtomicReferenceFieldUpdater]]
- [[AtomicStampedReference]]

==Better to return primitive value in methods, cause if not it can be set to any value with .set(n)==