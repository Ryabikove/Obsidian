конструкция, выполняющая определенный код в зависимости от аргумента, переданного конструкции

Конструкция имеет 2 типа синтаксиса:
```
switch(arg){ # первый
	case 1:
		System.out.print("Arg equal 1");
		break;
	case 2:
		System.out.print("Arg equal 2");
		int arg = 23;
		break;
	case 23:
		System.out.print("Arg equal 23");
		break;
	default:
		var arg1 = "default";
		System.out.print("Arg has default value");
		break;
}

switch(x){ # второй 
    case 1 -> System.out.print("Arg equal 1");  
    case 2 -> System.out.print("Arg equal 2");  
    case 23 -> System.out.print("Arg equal 23");  
    default -> System.out.print("Arg has default value");  
}
```

При использовании первого типа синтаксиса ключевое слово [[Java/constructions/control constructions/циклы/break|break]] необходимо для прерывания проверок, т.к. при удовлетворении одного условия, выполнятся все последующие до первого слова `break`.

Во втором случае используются [[Java/constructions/control constructions/Лямбда-выражения|лямбда-выражения]], внутри них нет необходимости использовать слова `break`, запись короче по сравнению с предыдущей.

Блок `default` выполняется в любом случае, когда до него доходит проверка внутри конструкции. Блок `default` не обязателен

#управляющая_конструкция #ключевое_слово #условная_операция 