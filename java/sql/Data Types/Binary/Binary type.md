Type ==bytea== is byte string with variable length, list of octets (bytes).
Instead of  string type, binary can:
 1. store bytes with value 0, «unprinable» characters and symbols of other encodings
	обычно это значения вне десятичного диапазона 32..126
 2. в операциях с двоичными строками обрабатываются байты в чистом виде
	текстовые строки обрабатываются в зависимости от языковых стандартов

==объем данных 1 или 4 байта + сама строка==

 поддерживает два формата ввода/вывода:
  - [[sql/Data Types/Binary/шестнадцатеричный|шестнадцатеричный]]
  - [[sql/Data Types/Binary/спецпоследовательностей|спецпоследовательностей]]
	традиционный для PostgreSQL формат 
входные данные принимаются в обоих форматах, выходные данные зависят от параметра конфигурации bytea_output
==в Postgresql по умолчанию выбран шестнадцатеричный==

cтандарт SQL определяет другой тип двоичных данных, BLOB (BINARY LARGE OBJECT). Его входной формат отличается от форматов bytea, но функции и операторы в основном те же.


[[sql/Data Types/Data Types|Data Types]]  [[sql/Data Types/Binary/непечатаемые символы|непечатаемые символы]]  [[sql/Data Types/Binary/bytea_output|bytea_output]]

#тип_данных  #бинарный_формат