Вспомогательный интерфейс, используемый для сбора потока в коллекцию.

Реализует методы:
- `toList()` - группирует эл-ты в список [[List]]
- `toSet()` - группирует эл-ты в множество [[Set]]
- `toCollection(*конструктор*)` - группирует эл-ты в указанную коллекцию
- `toMap()` - группирует эл-ты в множество [[java/пакет/встроенные/java.util/Map|Map]]
- `joining()` - соединяет эл-ты в один
- `groupingBy()` - группирует эл-ты из потока по признаку, возвращает эл-т типа [[java/пакет/встроенные/java.util/Map|Map]], может создать множество групп
	`groupingBy(Function classifier, Collector downstream)` 
	- classifier - параметр типа Function, возвращаемое значение которого будет выступать ключом в возвращаемом Map объекте метода
	- downstream - параметр типа Collector, который обрабатывает поток сгруппированных элементов и возвращает значения для Map объекта
- `partitioningBy()` - группирует эл-ты по условию на 2 группы `true` и `false`, возвращает эл-т типа [[java/пакет/встроенные/java.util/Map|Map]]
- `collectingAndThen()` - выполняет коллектор, после чего выполняет его преобразование.
	`collectingAndThen(Collector downstream, Function finisher)`
	- downstream - параметр типа Collector, который выполняется в самом начале
	- finisher - параметр типа Function, который обрабатывает возвращаемые в downstream значения.
- `counting()` - подсчитывает кол-во элементов
- `of()` - позволяет создать свой коллектор
```
Collector<A,B,C> collector = Collector.of(  # A - тип элемента в потоке, B - тип аккумулятора(промежуточный контейнер), C - тип результата
       B::new,  # Supplier<B> supplier - создает промежуточный контейнер
       (B,A) -> B.act(A),   # BiConsumer<B,A> accumulator - модифицирует B 
       (A, A) -> A  
       Collector.Characteristics.UNORDERED  
);
```

#интерфейс 