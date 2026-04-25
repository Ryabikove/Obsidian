Parent class with has general fields as id, create_at, update_at etc. It isn't saved in DB, but all child classes has its fields saved in own tables.

```
@MappedSuperclass
public abstract class BaseEntity {
	@Id
	@GeneratedValue(strategy = GenerationType.IDENTITY)
	private Long id;
	private LocalDateTime createdAt = LocalDateTime.now(); 
}

@Entity
public class User extends BaseEntity {
	private String email; // User already has id and createdAt
}
```