Class metadata is information about a [[Java/package/class/Class|class]] that the [[Java/tools/JVM|JVM]] stores internally, to understand how the class is structured and how to use it.

It isn't actual [[Java/package/built-in/java/lang/Object/Object|object]] data, but data about the class itself.

Metadata includes:
- Class name;
- [[Java/package/class/Field|Fields]]:
	- names;
	- [[sql/Data Types/Data Types|data type]];
	- access [[Java/variables/modifiers/Modifiers|modifiers]];
- [[Java/package/class/метод/Method|Methods]]:
	- method names;
	- return [[sql/Data Types/Data Types|data type]];
	- parameters;
- [[Java/package/class/метод/Constructor|Constructor]];
- [[Java/variables/modifiers/Modifiers|Modifiers]];
- Inheritate info:
	- [[Java/package/class/наследование/Наследование|Parent class]];
	- Implemented [[Java/package/class/наследование/интерфейс/interface|interfaces]];
- [[Annotations]];

Metadata is created in 2 steps:
- Class file is loaded by jvm;
- JVM extracts information and create metadata.

Stores in [[Java/memory/memory allocations/Method area (Metaspace)|Method area (Metaspace)]].