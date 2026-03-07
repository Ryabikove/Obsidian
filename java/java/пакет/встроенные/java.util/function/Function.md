[[java/пакет/класс/наследование/Функциональный интерфейс|Функциональный интерфейс]], позволяющий принимающий класс T и возвращающий класс R.

Реализовывает методы:
- `R apply(T t)` - участвует в лямбде;
- `default <V> Function<T, V> andThen(Function<? super R, ? extends V> after)` - получает на вход другую функцию и выполняет после основной
	`f.andThen(g).apply(val);`
- `default <V> Function<V, R> compose(Function<? super V, ? extends T> before)` - получает на вход другую функцию, и выполняет перед основной
	`f.compose(g).apply(val);`

Аналогичный интерфейс - [[java/пакет/встроенные/java.util/function/UnaryOperator|UnaryOperator]], только принимаемое и возвращаемое значение совпадают по типу.

Пример кода:
```
Function<Integer, String> length = s -> s.length(); 
int l = length.apply("Hello"); // 5
```


==В тернарной операции необходимо реализовать все 3 операнда, отсутствие одного из приведет к ошибке==

#интерфейс 