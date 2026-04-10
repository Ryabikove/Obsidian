преобразование значения одного типа в значение другого

There are 2 variants of convertion:
- automatic - during execution;
- manual - using special construction `int a = (int) b`.

Convertion при операциях (математических/логических):
- если один из операндов [[Java/variables/attributes/data type/primitive/float/Double|double]], то и второй операнд преобразуется к этому типу;
- если предыдущее условие ложно, а один из операндов [[Java/variables/attributes/data type/primitive/float/Float|float]], то и второй преобразуется к этому типу;
- если оба предыдущих ложны, и один из операндов [[Java/variables/attributes/data type/primitive/integer/Long|long]], второй преобразуется в long;
- иначе все операнды преобразуются к [[Java/variables/attributes/data type/primitive/integer/Int|int]].

==требования==:
 - значение преобразовываемого типа соответствует ограничениям преобразуемого типа по содержанию данных

==особенности==:
 - при преобразовании чисел с точкой к целым числам происходит потеря дробной части, во избегании потери применяют функцию округления
	double a = 56.9234;  int b = (int) a; System.out.print(b); \# 56
	int b = (int) Math.round(a); System.out.print(a); \# 57
 -  явные преобразования выполняются с помощью указания типа данных, к которому необходимо привести преобразование
	long a = 4;
	int b = (int) a;
 - автоматические преобразования могут быть только расширяющими
 - при преобразовании значения, выходящего за ограничения типа к которому преобразуют, произойдет потеря точности и данных
	int a = 258; byte b = (byte) a; System.out.print(b); \# 2
	a = 00000000 00000000 00000001 00000010; b = 00000010;
 - при преобразовании класса объекта методы и поля прошлого класса становятся недоступны
	 Class2 a; 
	 Class1 b = (Class1) a;

[[Java/variables/attributes/data type/type convertion/схема преобразования без потери точности.canvas|схема преобразования без потери точности]]
[[Java/variables/attributes/data type/type convertion/схема преобразования с потерей точности.canvas|схема преобразования с потерей точности]]
#тип_данных