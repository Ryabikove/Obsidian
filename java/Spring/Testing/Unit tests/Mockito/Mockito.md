Tool that is used for [[Spring/Testing/Unit tests/Unit tests|unit tests]] in spring apps.
It emulates dependecies which helps isolate units and simplify tests.

To emulate dependencies mockito uses **mock** - fake implementation of a class or interface that you can control and verify during tests. Main properties:
- has default return values (null, 0, false);
- return values may be specified;
- can show if methods were called;
- can throw exception when called;
To create **mock** annotation [[Spring/packages/org/mockito/Mock|Mock]] is used.

To inject mock into unit, we use [[Spring/packages/org/mockito/InjectMocks|InjectMocks]] annotation.

To specify tests units we use methods of class [[Spring/packages/org/mockito/Mockito|Mockito]], like `when` and `verify`.
```
verify(reposytory).save(any(Entity.class));
when(repository.save(any(Entity.class))).thenReturn(entity);
```

Checked methods may require or return some data. Sometimes it is important for us control type of this data.
In this cases we use methods of class [[Spring/packages/org/mockito/ArgumentMatchers|ArgumentMatchers]]. It tells to mockito, that we looking for specific data type but with any value. For example `any`: `any(Entity.class)`.
