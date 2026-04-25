Annotation maps field below with [[JPA/entity/annotations/column annotations/Embeddable|Embeddable]] class.

```
@Entity 
class User {
	@Embedded 
	private Address address;
}
```