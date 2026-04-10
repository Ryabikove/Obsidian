Serialization is a technology, which allows us save whole classes in files and download later. 
==Serialization is recursive==
==If serializable class has non-serializable object, java throws exception [[Java/package/built-in/java/io/NotSerializableException|NotSerializableException]]==

It has special requirenments:
- Saved class must implement [[Java/package/built-in/java/io/Serializable|Serializable]] interface (just marker);
- Use [[Java/package/built-in/java/io/ObjectOutputStream]] to save it;
- Use [[Java/package/built-in/java/io/ObjectInputStream]] to load it;

To prevent saving fields marker [[Java/memory/io streams/Transient|transient]] can be used (perfect for sensitive data or non-serializable).

To read and write objects we use:
- [[Java/package/built-in/java/io/ObjectOutputStream]]
```
try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("savegame.dat"))) {
    oos.writeObject(player); // Boom! Object is now a file.
}
```
- [[Java/package/built-in/java/io/ObjectInputStream]]
```
try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream("savegame.dat"))) {
    Hero loadedPlayer = (Hero) ois.readObject(); // Casting is required
    System.out.println("Loaded: " + loadedPlayer);
}
```

When you save object, change class and are trying to upload old object into a new class there would be [[Java/package/built-in/java/io/InvalidClassException]].
There is one more tool `serialVersionUID` - special field type long.
`private static final long serialVersionUID = 1L`
If serialVersionUID in file equals serialVersionUID in class, everything is okay.

*Main weaknesses*:
- Security - it's a common vector for "Remote Code Execution" attacks.
	Hacker can craft malicious byte streams that execute code when deserialized
- Size - the resulting files are mych larger than Jsonb or protobuf
- Regidity - it only works with java. You cant read java-serialized file easily in python or javascript

*Not all buil-in classes are serializable*
*Serializable:*
- Primitives and wrappers: [[Java/variables/attributes/data type/primitive/integer/Int|Int]], [[Java/package/built-in/java/lang/Integer|Integer]], etc;
- Text: [[Java/package/built-in/java/lang/String|String]], [[Java/package/built-in/java/lang/StringBuilder|StringBuilder]];
- Math: [[Java/package/built-in/java/math/BigDecimal|BigDecimal]], [[Java/package/built-in/java/math/BigInteger|BigInteger]];
- Collections: [[Java/package/built-in/java/util/ArrayList|ArrayList]], [[Java/package/built-in/java/util/HashMap|HashMap]], [[Java/package/built-in/java/util/HashSet|HashSet]], [[Java/package/built-in/java/util/LinkedList|LinkedList]].

*Non-serializable:*
- Threads: [[Java/package/built-in/java/lang/Thread|Thread]], [[Java/package/built-in/java/util/concurrent/ExecutorService|ExecutorService]];
- I/O: [[Java/package/built-in/java/io/InputStream|InputStream]], [[Java/package/built-in/java/io/OutputStream|OutputStream]], [[Java/package/built-in/java/io/FileDescriptor|FileDescriptor]];
- Network: [[Java/package/built-in/java/net/Socket|Socket]], [[Java/package/built-in/java/net/ServerSocket|ServerSocket]];
- GUI: many Swing and Javax components