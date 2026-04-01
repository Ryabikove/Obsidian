ключевое слово, объявляющее один класс наследником другого или один интерфейс наследником другого интерфейса

class Class1 {
	Type var1;
	Type var2;
	mod method1(type var){
		action
	}
}
class Class2 extends Class1{
	mod Class2(type var){
		super(var);
	}
}

interface inter1{}
interface inter2 extends inter1{}

[[Java/package/class/наследование/Наследование|Наследование]]
#класс #ключевое_слово