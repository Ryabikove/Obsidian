представляет ссылку на текущий экземпляр класса
через это слово можно обращаться к переменным, методам объекта, а так же вызывать его конструкторы

пример:
class Person{
	String name;
	int age;
	boolean baby;
	Person(){
		this("Undefined",18)
		this.check_age;
	}
	Person(String name, int age){
		this.name = name;
		this.age = age;
	}
	check_age(){
		this.baby = (age<18)?1:0;
	}
}

[[Java/package/class/метод/Constructor|Constructor]] [[Java/package/class/Class|Class]]
#класс #ключевое_слово