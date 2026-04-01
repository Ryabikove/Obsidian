Serialization is a technology, which allows us save whole classes in files and download later. 

It has special requirenments:
- Saved class must implement [[Java/package/built-in/java.io/Serializable|Serializable]] interface (just marker);
- Use [[ObjectOutputStream]] to save it;
- Use [[ObjectInputStream]] to load it;

To prevent saving fields marker [[Java/memory/io streams/Transient|transient]] can be used (perfect for sensitive data).

To read and write objects we use:
- [[ObjectOutputStream]]
```
try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("savegame.dat"))) {
    oos.writeObject(player); // Boom! Object is now a file.
}
```
- [[ObjectInputStream]]
```
try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream("savegame.dat"))) {
    Hero loadedPlayer = (Hero) ois.readObject(); // Casting is required
    System.out.println("Loaded: " + loadedPlayer);
}
```

When you save object, change class and are trying to upload old object into a new class there would be [[InvalidClassException]].
There is one more tool `serialVersionUID` - special field type long.
`private static final long serialVersionUID = 1L`
If serialVersionUID in file equals serialVersionUID in class, everything is okay.

*Main weaknesses*:
- Security - it's a common vector for "Remote Code Execution" attacks.
	Hacker can craft malicious byte streams that execute code when deserialized
- Size - the resulting files are mych larger than json or protobuf
- Regidity - it only works with java. You cant read java-serialized file easily in python or javascript