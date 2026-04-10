перечисление - не примитивный тип данных представляющий из себя упорядоченный список эл-тов (логически связанных констант)

enum Day{
	MONDAY,
	TUESDAY,
	WEDNESDAY,
	THURSDAY,
	FRIDAY,
	SATURDAY,
	SUNDAY
}

==особенности==:
 - может быть определена вне какого либо класса или метода
 - может содержать в себе конструкторы, поля и методы
	enum Color{
		RED("\#FF0000"), BLUE("\#0000FF"), GREEN("\#00FF00"); \# values
		private String code;   \# variable
		Color(String code){
			this.code = code;
		}
		public String getCode(){
			return code;
		}
	}
 - по умолчанию конструктор внутри перечисления приватный ([[Java/variables/modificators/private|private]])
 - можно определять методы для отдельных констант
	enum Test {
		TEST{
			public int action(int x, int y){return x+y;}
		}
	}


==требования==:
 - единственный разрешенный модификатор приватности конструктора - [[Java/variables/modificators/private|private]], использование других вызовет ошибку

==методы==:
 - [[Java/package/class/встроенные/enum/методы/values()|values()]] - возвращает все эл-ты в виде списка
 - [[Java/package/class/встроенные/enum/методы/ordinal()|ordinal()]] - возвращает порядковый номер константы (начинает с 0)

#переменная #тип_данных #ключевое_слово #комплексный_тип #класс