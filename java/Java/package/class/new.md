Keyword which creates a new [[Java/package/built-in/java/lang/Object/Object|object]] in memory.
There are [[Java/memory/Object|initialization]] and execution of [[Java/package/class/метод/Constructor|constructor]] in process of creating object.
Type val1 = new Type();

==особенности==:
 - при наследовании объекту базового класса можно передавать ссылку на объект производного, однако методы и поля производного будут недоступны (восходящее преобразование)
	 class Class2 extends Class1{} 
	 Class1 val1 = new Class2();
	 для нисходящего преобразования необходимо использовать операцию [[Java/variables/attributes/data type/type convertion/Type conversion|преобразования типов]]:
	 Class1 val2 = (Class1)val1;
 - в зависимости от того, какая ссылка будет передана экземпляру, такой метод и будет вызываться
	Class1 val1 = new Class2(); \# вызовется переопределенный метод из Class2
[[Java/package/class/Class|Class]] [[Java/package/class/наследование/Наследование|Наследование]]  [[Java/package/class/метод/переопределение методов|переопределение методов]]
#класс #ключевое_слово 