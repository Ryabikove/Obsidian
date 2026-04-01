Keyword that ensures visibility of changes to variables across [[Java/memory/threads/Thread|threads]].
It guarantees that the value of a variable will always be read from main memory, not CPU cache.

Example:
- `boolean keep = true;`
- thread A is running loop `while(keep) {...}`
- thread B changes `keep = false;`
- if `keep` isn't volatile, thread A might never stop, but if it is, thread A would stop as soon as B changes value.

How it works. The JVM sees volatile and understand that:
- Visibility - this variable doesn't need cache, every read and write must be done in RAM
- Ordering - no need to re-order instructions around this variable. It ensures that all writes made by thread A before setting the volatile flag are visible to thread B after it reads the flag.