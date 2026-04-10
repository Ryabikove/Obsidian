Local variables are declared inside a [[Java/package/class/метод/Method|method]], [[Java/package/class/метод/Constructor|constructor]] or [[Java/constructions/Code block|code block]].

Key features:
- Scope is limited to that method/block;
- Must be initialized before use;
- Stores in [[Java/package/built-in/java/util/Stack|Stack]];
- Not accessible outside the method.

```
class Class {
	method(){
		Type name = value; // local variable
	}
}
```