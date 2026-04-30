Main class of tool [[Spring/Testing/Unit tests/Mockito/Mockito|Mockito]] which contains methods to specify unit tests.

It has several methods:
- when(methodCall) - specifies return value of methods in mocked dependencies. without it return values in answer attribute of annotation [[Spring/packages/org/mockito/Mock|Mock]];
```
when(repository.findById(id)).thenReturn(Optional.of(entity));
```
- verify(mockObject).methodCall() - check if method of mocked dependecies was called.
```
verify(reposytory).save(any(Entity.class));
```