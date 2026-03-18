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
```
Collector.collectingAndThen(Collector.toList,
	list.stream()...
);
```

- `counting()` - подсчитывает кол-во элементов

- `teeing()` - разделяет поток на 2, после чего объединяет их в 1
	`teeing(Collector downstream1, Collector downstream2, BiFunction merger)` 
	- downstream1 - первый поток, в котором происходят какие-то действия
	- downstream2 - второй поток, в котором происходят какие-то действия
	- merger - функция, использующая результаты работы 2-х потоков и преобразующая их в другой результат
```
Collectors.teeing(  
       Collectors.minBy(Comparator.comparingDouble(Trade::price)),  
       Collectors.maxBy(Comparator.comparingDouble(Trade::price)),  
       (min, max) -> new TradeExtremes(min.get(), max.get())  
       )
```

- `summarizingDouble()` - принимающая поток числовых значений типа Double, и возвращающая статистическую информацию о числовых данных типа [[DoubleSummaryStatistic]].
	`summarizingDouble(ToDoubleFunction<? super T> mapper)`
	 - mapper - функция, извлекающая double значение из эл-та потока
```
DoubleSummaryStatistic stat = Collector.summarizingDouble(Class::getDouble)

stat.getMin(); getMax(); getAverage(); getCount(); getSum(); accept(); combine();
```

- `of()` - позволяет создать свой коллектор
```
Collector<A,B,C> collector = Collector.of( 
       B::new,  # Supplier<B> supplier - создает промежуточный контейнер
       (B,A) -> B.act(A),   # BiConsumer<B,A> accumulator - модифицирует B 
       (A, A) -> С  
       Collector.Characteristics.UNORDERED  
); # A - тип элемента в потоке, B - тип аккумулятора(промежуточный контейнер), C - тип результата
```

#интерфейс 