метод объекта [[Java/package/class/Scanner/объекты/in/in|in]] класса [[Java/package/class/Scanner/Scanner|Scanner]]

функционал: возвращение строки до первого пробела, введенной в консоли.
 Scanner in = new Scanner(System.in);
 System.out.print("Input a number: ");
 int num = in.next();
 System.out.printf("Your number: %s\\n", num);
 in.close();

[[Java/package/built-in/java/lang/String|String]]
#метод