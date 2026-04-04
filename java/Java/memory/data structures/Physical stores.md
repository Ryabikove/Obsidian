There are 4 main type of data structures which are about how to physically store data in memory.

[[Java/variables/атрибуты переменных/значения переменной/Array|Array]] is collection of items stored in contiguous memory location.
- *fixed size* which determinated when array is created;
- *fast access* to element by its index. O(1)

[[Java/package/built-in/java/util/LinkedList|LinkedList]] consists of "nodes". Each node contains two things: the actual data and a "pointer" (reference) to the next node in the sequence.
- *dynamic size*;
- *scattered memory* - nodes can be anywhere in memory and connected by links;
- *slower access* - searching value inside list has O(N) coefficient.

[[Java/package/built-in/java/util/ArrayList|ArrayList]] has inside an simple array, but manage to contain indefinite number of elements.
- *fast access* - cause it has simple array inside, we can find element by index O(1);
- *dynamic size* - inner array is still fixed-sized. But when it's limit reached, arraylist creates new array with size twice bigger, and copy all elements from old array to new;
- *loaded deletion* - when it needs to delete element in array list, after operation there are whole elements right from deleted should be shifted. O(N).

[[Java/package/built-in/java/util/HashMap|HashMap]] - collection that has unordered structure of key:value pares of data inside.
- *fast access* - it has almost O(1) coefficient of speed in searching algorithms. See [[Java/package/built-in/java/util/HashMap|Hash Collision]] for more information;
- *unordered* - data stores in pares key:value. Key musts be unique;
	When key is given, the hash function formats it into a specific integer. The int corresponds to an exact memory address (bucket).
- *dynamic size*;
- *simple deletion* - cause there is no order and fast access, every value can me deleted or modified with O(1) speed.