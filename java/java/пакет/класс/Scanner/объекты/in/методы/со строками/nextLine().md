kметод объекта [[пакет/класс/Scanner/объекты/in/in|in]] класса [[пакет/класс/Scanner/Scanner|Scanner]]

функционал: возвращение всей строки, введенной в консоли.
 Scanner in = new Scanner(System.in);
 System.out.print("Input a number: ");
 int num = in.nextLine();
 System.out.printf("Your number: %s\\n", num);
 in.close();

[[java/пакет/встроенные/java.lang/String|String]]
#метод