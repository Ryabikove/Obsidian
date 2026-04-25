Annotation get used in conjunction with the [[JPA/entity/annotations/column annotations/Id|@Id]] annotation to automatically generate unique values.
Optional annotation.

Has several attributes:
- strategy - provides several strategies of value generations:
	- GenerationType.IDENTITY - relies on the database's auto-increment feature
	- GenerationType.SEQUENCE - users a database sequence (Oracle, PostgreSQL), requires a sequence object in the database
	- GenerationType.TABLE - uses a separate table to simulate sequences, works across all databases but has performance overhead
	- GenerationType.AUTO - lets the jpa provider choose the best strategy based on the database
	- GenerationType.UUID - generates a Universally Unique Identifier (UUID) compliant with RFC 4122, Ideal for distributed systems where uniqueness across databases is required.

```
@Id
@GeneratedValue(strategy = GenerationType.IDENTITY)
private short id;  
```