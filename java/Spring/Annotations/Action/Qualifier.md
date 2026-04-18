Annotation, which is used to specify [[Spring/Entitites/Bean|Bean]] that should be wired with [[Spring/Annotations/Action/Autowired|Autowired]].
```
@Bean
class Bean0 implements Intface

@Bean
class Bean1 implements Intface

class Main {
	@Autowired
	@Qualifier("bean0")
	Intface var;
}
```