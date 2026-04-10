класс - основная комплексная единица кода в java, шаблон написания [[Java/package/built-in/java/lang/Object/Object|object]].

в состав класса входят:
 - [[Java/package/class/метод/Method|методы]]
 - [[Java/package/class/Attribute|атрибуты]]

синтаксис определения:
```
 *modificators* class  Class_name {
	 *block of code*
}
```
[[Java/variables/modificators/Modificators|Modificators]]  [[Java/constructions/Code block|Code block]]

==требования==:
 - главный класс любой программы на java ==должен== содержать метод [[Java/package/class/метод/main]]
 - название файла и главного класса в файле ==должны== совпадать

==особенности==:
 - для создания объекта используется оператор [[Java/package/class/New|New]]
 - при создании объекта определенного класса вызывается [[Java/package/class/метод/Constructor|Constructor]] - специальный метод [[Java/memory/Object|initializes object]];
 - классы могут объединяться в пакеты
 - в java присутствуют встроенные классы
 - Один класс может [[Java/package/class/наследование/Наследование|наследоваться]] от другого
 - помимо базовых классов есть абстрактные классы [[Java/variables/modificators/abstract|abstract]]
	абстрактный класс отличается от обычного тем, что нельзя использовать его конструктор напрямую, а только через производный класс. основная задача абстрактного класса - быть унаследованным производным классом
 - класс может быть определен внутри другого класса или интерфейса
	[[Java/package/class/Inner classes|Inner classes]]
 - при написании класса можно задать универсальный параметр, позволяющий определять тип полей класса при создании экземпляра - обобщенный класс
	[[Java/package/class/обобщения/generics-обобщения|generics-обобщения]]

[[Java/package/импорт классов и пакетов|импорт классов и пакетов]]