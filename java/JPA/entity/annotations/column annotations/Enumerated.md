Annotation maps field below with [[Java/package/class/встроенные/enum/enum|enum]] values.

It has several types of storing:
- STRING - persist enumerated type property or field as a string. The enumerated value inside table equals to Enum.name() value;
	May be broken cause of changing enum values;
- ORDINAL (By default) - persist enumerated type property or field as an integer. The enumerated value inside table equals to Enum.ordinal() value;
	Not recommended cause may be broken because of putting new value into enum not in the end.

```
public enum Role { ADMIN, USER }
@Entity
public class User {
    @Enumerated(EnumType.STRING)
    private Role role;
}
```