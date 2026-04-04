Phisycal flows (streams) of data in programm. Don't confuse with [[Java/constructions/управляющие конструкции/Stream-api/Stream-api|stream-api]], it is not the same streams.
Input - stream from data storage  to process.
Otput - stream from process to data storage.

Data storage can be file, another programm, database, internet and so on.
Streams can be determinated by flowing data:

| *Feature*      | *Byte Streams*                                                                                                            | *Character Streams*                                                                                 |
| -------------- | ------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| *Data Type*    | Raw 8-bit bytes (0-255)                                                                                                   | 16-bit Unicode characters                                                                           |
| *Best For*     | Images, Videos, Zip files, Executables                                                                                    | Text files, Logs, HTML, JSON                                                                        |
| *Root Classes* | [[Java/package/built-in/java/io/InputStream\|InputStream]] / [[Java/package/built-in/java/io/OutputStream\|OutputStream]] | [[Java/package/built-in/java/io/Reader\|Reader]] / [[Java/package/built-in/java/io/Writer\|Writer]] |

There are 2 patterns to make streams.
*Decoration pattern*:
To read data from file there are 3 different classes needed.
```
FileInputStream fis = new FileInputStream("data.txt"); // Raw bytes from file
BufferedInputStream bis = new BufferedInputStream(fis); // Adds a buffer (faster!)
DataInputStream dis = new DataInputStream(bis); // Allows reading ints, doubles, etc.
```

[[Java/package/built-in/java/io/BufferedInputStream|BufferedInputStream]] makes reading faster cause it no longer needs to ask hard drive for one byte, it just asks for whole data and store into buffer.

*Modern way*:
Starting with Java 7, the new I/O classes become available.
Main classes:
- [[Java/package/built-in/java/io/file/Path|Path]] - location of file;
- [[Java/package/built-in/java/io/file/Paths|Paths]]/[[Java/package/built-in/java/io/file/Path|Path.of]] - how create a Path;
- [[Java/package/built-in/java/io/file/Files|Files]] - utility class which does main actions (read, write, delete, copy);

```
String content = Files.readString(Path.of("./data.txt")); // read data
Files.write(Path.of("output.txt"), List.of("Line 1", "Line 2")); //write data
```


There is [[Java/memory/io streams/Serialization|serialization]] technology, which allows us save whole classes in files and download later.

IO can be [[Java/memory/io streams/Blocking and non-blocking|blocking and non-blocking]]:
- blocking - wait until data be read or written
- non-blocking - wait a signal and do another things at the same time