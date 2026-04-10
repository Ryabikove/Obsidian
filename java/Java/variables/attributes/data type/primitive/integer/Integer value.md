Integer number values like:
 - [[Java/variables/attributes/data type/primitive/integer/Int|int]];
 - [[Java/variables/attributes/data type/primitive/integer/Short|short]];
 - [[Java/variables/attributes/data type/primitive/integer/Byte|byte]];
 - [[Java/variables/attributes/data type/primitive/integer/Long|long]].
 

==Without specifying a type, all integer values ​​default to the int type.
If the range of int values ​​is exceeded, the compilation attempt will fail. To compile correctly, append L or l to the end of the integer.==
```
long num = 2147483649l
```

Values ​​for integer variables can be specified not only in base 10, but also in base 2, base 8, and base 16. To ensure the compiler understands the base 10, a prefix is ​​added before the number.
```
0 - 8-th: int x=010 # 8 in 8-th
0х - 16-th: int x=0x6F # 16 in 16-th
0b - 2-d: int x=0b1101 # 13 in 2-d
```

The digits of a number can be separated by the "\_" sign:
```
int x = 123_123 \# 123123
```

[[Java/variables/attributes/data type/Nember with character|Nember with character]] 
#переменная  #целое_число
