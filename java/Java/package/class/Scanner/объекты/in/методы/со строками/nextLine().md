kметод объекта [[Java/package/class/Scanner/объекты/in/in|in]] класса [[Java/package/class/Scanner/Scanner|Scanner]]

функционал: возвращение всей строки, введенной в консоли.
 Scanner in = new Scanner(System.in);
 System.out.print("Input a number: ");
 int num = in.nextLine();
 System.out.printf("Your number: %s\\n", num);
 in.close();

[[Java/package/built-in/java/lang/String|String]]
#метод