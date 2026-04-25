Java class, marked with "[[JPA/entity/annotations/Entity|@Entity]]" annotation, which is translated by JPA as table structure.

JPA map class to table with the same name and in default DB schema. If you want specify info you should use annotation [[JPA/entity/annotations/table annotations/Table|@Table]]
- It is optional annotation and without it JPA anyway try to map class and table.

Annotation [[JPA/entity/annotations/column annotations/Column|@Column]] is used to map [[Java/package/class/Field|field]] in class to specific column in table:
- Table may have no mapped fields but [[sql/Data Base/Schema/Table/Column/Modificators/Primary key|primary key]].

To mark field as [[sql/Data Base/Schema/Table/Column/Modificators/Primary key|primary key]] annotation [[JPA/entity/annotations/column annotations/Id|@Id]] is used:
- It is essential annotation and must be only one per class. *Whithout it table won't be created.*

Entity may have special common class which describes several fields from table.
These classes are made with annotation [[JPA/entity/annotations/column annotations/Embeddable|Embeddable]] and [[JPA/entity/annotations/column annotations/Embedded|Embedded]]. It makes code mode simple and group fields by meaning.

```
@Entity 
class User {
	@Embedded 
	private Address address;
}
```

JPA has special ingeritance mapping ways:
- SINGLE_TABLE (By default) - all child classes stores in single table and defined by special column "DTYPE" which contains class identification.
- JOINED - parent class is stored in one table and specific fields of child classes are stored in other tables.
- TABLE_PER_CLASS - every child class has own independent table.

Enumerated values also can be stored in DB with JPA. [[JPA/entity/annotations/column annotations/Enumerated|@Enumerated]] annotation is used to mark field as enum type.

Entity may have [[JPA/entity/MappedSuperclass|MappedSuperclass]] - class which isn't saved in DB, but its fields are saved in child entity table.

Specific annotations and meanings:


- [[JPA/entity/annotations/column annotations/GeneratedValue|@GeneratedValue]] - optional annotation get used in conjunction with the @Id annotation to automatically generate unique values;

- [[JPA/entity/annotations/relate annotations/OneToOne|@OneToOne]]
- [[JPA/entity/annotations/relate annotations/ManyToOne|@ManyToOne]]
- [[JPA/entity/annotations/relate annotations/OneToMany|@OneToMany]]
- [[JPA/entity/annotations/relate annotations/ManyToMany|@ManyToMany]]