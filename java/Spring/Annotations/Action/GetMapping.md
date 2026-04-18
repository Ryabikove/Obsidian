Annotation, which used inside [[Spring/Entitites/RestController|RestController]] to tell Spring which method is triggered by specific url.

```
@RestController
class RestController {
	@GetMapping
	public Type method()
}
```