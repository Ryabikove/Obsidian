Вспомогательный интерфейс, используемый для сбора потока в коллекцию.

Реализует методы:
- `toList()` - группирует эл-ты в список [[Java/package/built-in/java/util/List]]

- `toSet()` - группирует эл-ты в множество [[Java/package/built-in/java/util/Set]]

- `toCollection(*конструктор*)` - группирует эл-ты в указанную коллекцию

- `toMap()` - группирует эл-ты в множество [[Java/package/built-in/java/util/Map|Map]]

- `joining()` - соединяет эл-ты в один

- `reducing()` - объединяет элементы коллекции попарно и возвращает Optional\<A>
	reducing([[Java/package/built-in/java/util/function/BinaryOperator|BinaryOperator]] op)
	- op\<A> - функция, принимающая на вход пару значения A и объединяющая их
```
Collector.reducing((left,right) -> {
	left.addAll(right);
	return left;
	}
);
```
- `groupingBy()` - группирует эл-ты из потока по признаку, возвращает эл-т типа [[Java/package/built-in/java/util/Map|Map]], может создать множество групп
	groupingBy([[Java/package/built-in/java/util/function/Function|Function]] classifier, Collector downstream) 
	- classifier - параметр типа Function, возвращаемое значение которого будет выступать ключом в возвращаемом Map объекте метода
	- downstream - параметр типа Collector, который обрабатывает поток сгруппированных элементов и возвращает значения для Map объекта

- `partitioningBy()` - группирует эл-ты по условию на 2 группы `true` и `false`, возвращает эл-т типа [[Java/package/built-in/java/util/Map|Map]]

- `collectingAndThen()` - выполняет коллектор, после чего выполняет его преобразование.
	collectingAndThen(Collector downstream, [[Java/package/built-in/java/util/function/Function|Function]] finisher)
	- downstream - параметр типа Collector, который выполняется в самом начале
	- finisher - параметр типа Function, который обрабатывает возвращаемые в downstream значения.
```
Collector.collectingAndThen(Collector.toList,
	list.stream()...
);
```

- `counting()` - подсчитывает кол-во элементов

- `teeing()` - разделяет поток на 2, после чего объединяет их в 1
	teeing(Collector downstream1, Collector downstream2, [[BiFunction]] merger) 
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
	summarizingDouble(ToDoubleFunction\<? super T\> mapper)
	 - mapper - функция, извлекающая double значение из эл-та потока
```
DoubleSummaryStatistic stat = Collector.summarizingDouble(Class::getDouble)

stat.getMin(); getMax(); getAverage(); getCount(); getSum(); accept(); combine();
```

- `of()` - позволяет создать свой коллектор
	of([[Java/package/built-in/java/util/function/Supplier|Supplier]] supplier, [[BiConsumer]] accumulator, [[Java/package/built-in/java/util/function/BinaryOperator|BinaryOperator]] combiner, \[[[Java/package/built-in/java/util/function/Function|Function]] finisher], \[Collector.Characteristics])
	- supplier\<B> - создает промежуточный тип хранения данных контейнер B
	- accumulator\<B,A> - добавляет входные эл-ты A в контейнер B
	- combiner\<B> - объединяет эл-ты B
	- finisher\<B,C> - если тип B и тип C совпадают, то оператор не обязательный. Преобразует B в C. Может использоваться так же для проверки результата.
	- Characteristics - необязательный оператор, указывающий на дополнительные св-ва коллектора
		- CONCURRENT - означает, что контейнер типа C может поддерживать накопление из нескольких параллельных потоков. Если коллектор не является так же UNORDERED, то его следует использовать только для неупорядоченных источников данных.
		- UNORDERED - означает, что накопление не требует сохранения порядка входных данных. Т.е. тип C не является упорядоченным или зависящим от порядка накопления.
		- IDENTITY_FINISH - означает, что finisher является **Identity**(ничего не выполняет) и может быть отключена. Используется в случае, если преобразование от промежуточного контейнера к конечному всегда успешно.
```
Collector<A,B,C> collector = Collector.of( 
       B::new,
       (B,A) -> B.act(A),    
       (B,B) -> B+B,
       (B,C) -> C.of(B),
       Collector.Characteristics.Characteristics  
);
```

#интерфейс 