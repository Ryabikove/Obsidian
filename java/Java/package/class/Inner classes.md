классы могут быть внутренними, т.е. определенными внутри другого класса.
Существует 4 разновидности таких классов:
1. Вложенный класс (inner) - обычный класс внутри другого
```
class Outer_class{
	Inner_class var;
	Outer_class{
		this.var = new Inner_class(val);
	}
	
	class Inner_class{...}
}
```
Такой класс имеет доступ ко всем полям внешнего класса, даже к [[Java/variables/modificators/private|private]]. Внешний класс так же имеет доступ ко всем полям внутреннего класса, даже закрытым модификатором private

2. Статический вложенный класс (static netsted class) - тот же inner, но с модификатором [[Java/variables/modificators/static|static]]. 
```
class Outer_class{
	Inner_class var;
	Outer_class{
		this.var = new Inner_class(val);
	}
	
	static class Inner_class{...}
}
```
В отличие от предыдущего, он не привязан к конкретному экземпляру внешнего класса, а является общим для всех и не имеет доступа к нестатичным полям. Так же статические классы потребляют меньше памяти, т.к. не хранят скрытую ссылку на объект внешнего класса.
Простой способ логически сгруппировать классы.

3. Локальный класс (local class) - описывается прямо внутри метода и виден только внутри этого метода.
Используется крайне редко, в основном когда нужно создать вспомогательный тип для сложной логики "здесь и сейчас".
```
class Outer_class{
	public void method(){	
		class Inner_class{...}
		Inner_class var = new Inner_class();
	}
}
```

4. Анонимный класс (anonymous class) - класс без имени. Одновременно объявляется и создается объект. Анонимный класс создается только из абстрактного или интерфейса. Все поля и методы анонимного класса доступны вовне, только если объявлены в интерфейсе.
```
interface Validator { boolean isValid(String value); }

Validator nameValidator = new Validator() { 
	@Override public boolean isValid(String value) { 
		return value != null && value.length() > 2; 
	} 
};
```
Именно из анонимных классов выросли [[Java/constructions/control constructions/Лямбда-выражения]]. В современном коде вместо 5 строк анонимного класса пишут одну: 
`value -> value.length() > 2`.
Анонимные классы часто встречаются в проектах, особенно при сортировке [[Study/1 java core/5 Collections|коллекций]]. Пример с сортировкой:
```
items.sort(new Comparator<Item>() { 
	@Override 
	public int compare(Item o1, Item o2) { 
		return o1.weight - o2.weight; // Сортировка по возрастанию 
	} 
});
```


==особенности==:
 - объект внутреннего класса можно объявить внутри любого контекста, в том числе метода или цикла
 - все указанное так же относится и к интерфейсам

ссылку на объект внешнего класса из внутреннего класса можно получить с помощью выражения: Outer_class.this
[[Java/package/class/Class|Class]]
#класс #интерфейс 