Annotation, which wire [[Spring/Entitites/Bean|beans]] with its object in main class.

If there are several beans with same interface, spring couldn't decide which to use. Annotation [[Spring/Annotations/Action/Qualifier|Qualifier]] is used to tell spring which exact bean it should use.

==Bean must implements interface which used as type of the object in main class==

```
@Bean
class Bean implements Intface

class Main {
	@Autowired
	Intface var;
}
```