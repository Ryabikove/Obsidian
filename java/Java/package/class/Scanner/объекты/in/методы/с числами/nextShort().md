метод объекта [[Java/package/class/Scanner/объекты/in/in|in]] класса [[Java/package/class/Scanner/Scanner|Scanner]]

функционал: возвращение числа типа [[Java/variables/attributes/data type/primitive/integer/Short|Short]], введенного в консоли.
 Scanner in = new Scanner(System.in);
 System.out.print("Input a number: ");
 int num = in.nextShort();
 System.out.printf("Your number: %s\\n", num);
 in.close();


#метод