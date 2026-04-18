Essential ecosystem for Java development. It handles the repetitive, underlying infrastructure of an application, like security, database connections and web request routing.

The absolute foundation of Spring is a concept called *Dependency Injection* - the main concept which create dependency automatically.
There are 2 types of dependency injection:
1. By field directly - with annotation [[Spring/Annotations/Action/Autowired|Autowired]];
2. By constructor - more reliable and testable
	- You can mark object in class as [[Java/variables/modifiers/final|final]];
	- You can not create onject without dependency;
	- You can change repo with only one construction: `new Service(mockRepo)`.

The main entity in Spring is [[Spring/Entitites/Bean|bean]]. Other entities based on it, like:
- [[Spring/Entitites/Reposytory|Reposytory]];
- [[Spring/Entitites/RestController|RestController]];
- [[Spring/Entitites/Service|Service]].

There is also [[Spring/Entitites/Configuration|configuration]] entity which stores beans.

To find all labels spring uses process *Component Scanning*. It starts at a specific folder with annotation [[Spring/Annotations/Entity/SpringBootApplication|SpringBootApplication]] and looks at everything inside it and its sub-folders.

To handle this setup automatically we use [[Spring/Spring Boot|Spring Boot]] - the main part of ecosystem which reduce initial setup by providing sebsible, pre-configured defaults.

Spring also provides [[Spring/Testing/Testing|automatic testing tools]].