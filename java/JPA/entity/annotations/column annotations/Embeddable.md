Annotation maps class below to field with [[JPA/entity/annotations/column annotations/Embedded|@Embedded]] annotation.

Embeddable class has fields and no id. Behaviour of fields inside same as fields inside [[JPA/entity/Entity|Entity]]. But it allows us group fields inside simplier class by meaning.

```
@Embeddable
class Address {
	private String city;
	private String street;
	private String zipCode;
} 
```