[[Java/package/class/наследование/Функциональный интерфейс|Функциональный интерфейс]], позволяющий получить новый объект.

Реализует единственный метод - T get();

Пример кода:
```
Supplier<Object> newObject = () -> new Object(); 
Object result = newObject.get(); // true
```

#интерфейс 