[[Java/package/class/наследование/Функциональный интерфейс|Функциональный интерфейс]], позволяющий реализовывать проверку с помощью лямбда выражений.
Принимается всегда в методе в [[Java/constructions/управляющие конструкции/Stream-api/Stream-api|stream-api]]

Реализует единственный метод - boolean test(T t);

Пример кода:
```
Predicate<String> isNotEmpty = s -> !s.isEmpty(); 
boolean result = isNotEmpty.test("Hello"); // true
```

#интерфейс 