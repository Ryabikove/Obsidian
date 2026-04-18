Java Native Interface. Special tool which is used as handles by native code (like C/C++) to access Java object safely.

Java runs code inside [[Java/tools/JVM|JVM]], which has isolated memory. Native code cannot directly use raw memory addresses of Java objects, it uses JNI, which provide safe references.

There are 3 type of references:
- Local - created automatically inside a native method and valid only during execution of that method. When method ends, reference is automatically destroyed.
- Global - created explicitly using JNI functions and valid across multiple native method calls. Must be manually freed.
- Weak Global - similar to global references, but don't prevent [[Java/memory/memory allocations/Garbage collector|GC]].

Whith JNI and its references we can:
- Prevent memory corruption;
- Work safely with GC;
- Allow java < - > C/C++ interaction.