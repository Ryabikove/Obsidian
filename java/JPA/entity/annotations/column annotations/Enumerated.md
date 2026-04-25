Annotation maps field below with [[Java/package/class/встроенные/enum/enum|enum]] values.

It has several types of storing:
- STRING - more reliable way to store

```
public enum Role { ADMIN, USER }
@Entity
public class User {
    @Enumerated(EnumType.STRING)
    private Role role;
}
```