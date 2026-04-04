Класс, реализующий неупорядоченную коллекцию элементов ключ:значение.

Ключи должны быть уникальными, но значения могут повторяться.
Использует [[Java/package/class/обобщения/generics-обобщения|обобщения]] для указания класса, который будет хранить.

When key is given, the hash function formats it into a specific integer. The int corresponds to an exact memory address (bucket).
The hash function can give one same value to different keys - it's called *Hash Collision*:
- Key is formatted into hash
- Memory slot for this hash has already been taken
- There is [[Java/package/built-in/java/util/LinkedList|LinkedList]] created on this slot
- When we need one of these keys, java goes to the slot, sees linked list, goes through it until finds needed value
Despite searching slot is fast as O(1), searching value in linked list is slower as O(N).
==In modern java if collision chain gets too long (usually more than 8 items) - Java upgrades linked list into [[Red-Black Tree]] to make it faster.==


Методы:
- `map.put(key, value)` — добавить.
- `map.get(key)` — получить (вернет `null`, если ключа нет).
- `map.containsKey(key)` — проверить наличие ключа.
- `map.entrySet()` - возвращает множество ключ:значение
	позволяет перебирать коллекцию через циклы
```
for (Map.Entry<String, Book> entry : map.entrySet()) { 
	System.out.println("ISBN: " + entry.getKey() + " | Название: " + entry.getValue().getTitle()); 
}
```

Наследуется от [[Java/package/built-in/java/util/Map|Map]]

#коллекция #класс 