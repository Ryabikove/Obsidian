Phisycal flows (streams) of data in programm. Don't confuse with [[Java/constructions/управляющие конструкции/Stream-api/Stream-api|stream-api]], it is not the same streams.
Input - reading data into your programm.
Otput - writing data out of your programm.

Streams can be determinated by flowing data, root classes and best uses:
- byte
- character

Also there are few patterns how to make streams:
- Decoration pattern - need a lot of lightweight objects to make stream
```
FileInputStream fis = new FileInputStream("data.txt"); // Raw bytes from file
BufferedInputStream bis = new BufferedInputStream(fis); // Adds a buffer (faster!)
DataInputStream dis = new DataInputStream(bis); // Allows reading ints, doubles, etc.
```
- Modern way - need less classes to do same things
	become available with Java 7
```
String content = Files.readString(Path.of("./data.txt")); // read data
Files.write(Path.of("output.txt"), List.of("Line 1", "Line 2")); //write data
```

Java has [[Java/memory/io streams/Serialization|serialization]] technology which allows us save whole classes into files and download later.
To prevent saving fields keyword [[Java/memory/io streams/Transient|transient]] can be used (perfect for sensitive or non-serializable data).

For more information see [[Java/memory/io streams/Input-Output streams|I/O streams]].