В java можно определять класс внутри другого, тем самым создавая [[Java/package/class/Inner classes|Inner classes]]. Это полезно, когда один класс нужен только внутри другого и нигде больше.

Существует 4 разновидности таких классов:
1. Вложенный класс (inner) - обычный класс внутри другого
2. Статический вложенный класс (static netsted class) - тот же inner, но с модификатором [[Java/variables/modifiers/static|static]]. 
3. Локальный класс (local class) - описывается прямо внутри метода и виден только внутри этого метода.
4. Анонимный класс (anonymous class) - класс без имени. Одновременно объявляется и создается объект.

Любая вложенность обусловлена специфическими потребностями в экономии памяти или ограничении видимости:
1. inner class - когда класс используется только одним классом и ничем больше, и когда класс не может существовать отдельно. При этом функционал вложенного класса недостаточно обширный, чтобы выносить его вовне.
```
class Library { 
	private String name = "Центральная";
	
	class Librarian { 
		void work() { // Имеет доступ к полю name внешнего класса!
		System.out.println("Я работаю в библиотеке: " + name); 
		}
	} 
} 

// Чтобы создать Библиотекаря, НУЖЕН объект Библиотеки: 
Library lib = new Library(); 
Library.Librarian emp = lib.new Librarian();
```

2. static nested class - если внутренний класс может существовать отдельно от конкретных экземпляров внешнего, но должен быть общим для всего внешнего класса. 
```
class Book {
    static class BookHelper {
        void help() { System.out.println("Я просто помогаю, мне не нужна сама книга"); }
    }
}
// Можно создать без объекта Book:
Book.BookHelper helper = new Book.BookHelper();
```

3. local class - используется, если внутри метода используется сложный функционал, но нигде больше он не нужен. Основной класс не раздувается методами. Так же локальный класс имеет доступ к переменным метода (если они `effectively final`)
```
public void processComplexOrder(Order order) {
    // Локальный класс для временных расчетов
    class DiscountCalculator {
        double base = 0.1;
        
        double getSeasonal() { return order.isWinter() ? 0.05 : 0; }
        double getLoyalty() { return order.getUser().isVip() ? 0.1 : 0; }
        
        double total() { return base + getSeasonal() + getLoyalty(); }
    }

    DiscountCalculator calc = new DiscountCalculator();
    order.setPrice(order.getPrice() * (1 - calc.total()));
}

public Runnable createPrinter(String message) {
	class Printer implements Runnable {
		@Override
		public void run() { 
			// Магия: метод createPrinter уже завершился, 
			// но объект Printer всё еще помнит переменную message!
			System.out.println(message);
		}
	}
	return new Printer(); 
}
```

4. anonymous class - используются, когда лямбда-выражения не могут быть использованы, а создание отдельного класса - неоправданное усложнение кода. Анонимные классы часто встречаются в проектах, особенно при сортировке [[Study/1 java core/5 Collections|коллекций]].
```
items.sort(new Comparator<Item>() { 
	@Override 
	public int compare(Item o1, Item o2) { 
		return o1.weight - o2.weight; // Сортировка по возрастанию, но лямбда выражение лучше
	} 
});
```
Именно из анонимных классов выросли [[Java/constructions/control constructions/Лямбда-выражения|Лямбда-выражения]]. В современном коде вместо 5 строк анонимного класса пишут одну: 
`value -> value.length() > 2`.
Лямбда выражения бессильны в следующих случаях:
- необходимо реализовать более 1 метода
```
button.addMouseListener(new MouseListener() {
	public void mouseClicked(MouseEvent e) { System.out.println("Клик!"); }
    public void mousePressed(MouseEvent e) {}
    public void mouseReleased(MouseEvent e) {}
    public void mouseEntered(MouseEvent e) { System.out.println("Мышь вошла в зону"); }
    public void mouseExited(MouseEvent e) {}
});
```
- необходимо наследоваться от другого класса
```
Book secretBook = new Book("Тайные знания", "Неизвестен", 500) {
    @Override
    public String getAuthor() {
        return "**********"; // Скрываем автора только для этого объекта
    }
};
```



==особенности==:
 - объект внутреннего класса можно объявить внутри любого контекста, в том числе метода или цикла
 - все указанное так же относится и к интерфейсам

ссылку на объект внешнего класса из внутреннего класса можно получить с помощью выражения: Outer_class.this
[[Java/package/class/Class|Class]]
#класс #интерфейс 