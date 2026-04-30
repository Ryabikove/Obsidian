Annotation, from [[Spring/Testing/Unit tests/Mockito/Mockito|Mockito]] which is used to create mock objects for unit testing.
It replace real dependencies by simulating it.

It has several attributes:
- name - specify name of the mock in logs and debug (By default - generated);
- answer - specify default answer for unstubbed methods (By default - [[Spring/packages/org/mockito/Answers|Answers.RETURNS_DEFAULTS]]);
- stubOnly - specify whether mock should be stub-only without verification (By default - false);
- extraInterfaces - specify additional interfaces for the mock to implement (By default - empty);
- serializable - specify whether mock should be serializable (By default - false);
- lenient - specify whether mock should be lenient whithout strict stubbing (By default - false);

```
@Mock
Reposytory reposytory;
```