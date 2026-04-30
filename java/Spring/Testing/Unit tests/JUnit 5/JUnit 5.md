Tool which is used like engine for [[Spring/Testing/Unit tests/Unit tests|unit tests]] in spring apps.

It runs tests and check results if it is okay. We use annotation [[Spring/packages/org/junit/jupiter/api/Test|Test]], to mark methods as testing scenario.
```
@Test
public void Test1(){...}
```

A scenario may be positive, when we check correct execution, and negative, when we check incorrect execution (exception throws). 
Positive checking enabled and executed by default.
For negative scenario we use method `assertThrows()` of class [[Spring/packages/org/junit/jupiter/api/Assertations|Assertations]].
```
assertThrows(EntityNotFoundException.class, () -> service.findById("999"));
```