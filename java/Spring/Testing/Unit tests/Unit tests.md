Unit tests - tests that are focused on testing single **unit** of code in complete isolation.

Usually **unit** is a single class (like [[Spring/Entitites/Service|Service]]).
The goal of this tests is to verify the logic inside units without worrying about external factors like file system, database or other services.

To achive isolation, two primary tools are used:
- [[Spring/Testing/Unit tests/Mockito/Mockito|Mockito]] - emulator of dependencies;
- [[Spring/Testing/Unit tests/JUnit 5/JUnit 5|JUnit 5]] - engine that runs the tests and checks reuslts if it's correct;

Mockito is responsible for dependencies, its calls and insert/return values.
So we can specify with it:
- which dependency must be emulated;
- which methods will be called;
- which data types and values will be inserted in methods or returned from it;

JUnit responsible for launching testing scenario, negative testing