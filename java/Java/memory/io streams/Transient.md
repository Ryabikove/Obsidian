Keyword which marked fields in class that should not be saved in [[Java/memory/io streams/Serialization|serializable]] class.
(Like a password, secret key or non-serializable classes)

In process of serialization java ignores this fields and after deserialization this fields equal [[null]] of default value for primitives.

Example:
```
// 2. This field will NOT be saved!
private transient String password;
```