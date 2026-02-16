метод объекта [[пакет/класс/Scanner/объекты/in/in|in]] класса [[пакет/класс/Scanner/Scanner|Scanner]]

функционал: возвращение значения типа [[переменные/атрибуты переменных/типы данных/целочисленные/byte|byte]], введенного в консоли.
 Scanner in = new Scanner(System.in);
 System.out.print("Input a number: ");
 int num = in.nextByte();
 System.out.printf("Your number: %s\\n", num);
 in.close();

#метод