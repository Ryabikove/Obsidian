Built-in class is used for thread creation.
Implement interface [[Java/package/built-in/java/lang/Runnable|Runnable]].

Defines [[Java/package/class/метод/конструктор|constructors]] and [[Thread.Builder]] to create threads. 

Defines methods:
- start() - execute thread
	```
	public void start() {
		synchronized (this) {
			// zero status corresponds to state "NEW".
			if (holder.threadStatus != 0) {
				throw new IllegalThreadStateException();
			}
			start0(); 
	}
	```
- start0() - not intended to be invoke directly, executed by `start()`
	`private native void start0();`

[[Java/memory/threads/Syncronized]]

#класс 