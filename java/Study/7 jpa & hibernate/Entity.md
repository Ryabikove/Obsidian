Java class, marked with "@Entity" annotation, which is translated by JPA as table structure.

This class has scpecial fields and annotations:
```
@Entity  
@Table(name = "corporations") 
public class Corporation {  
    @Id  
    @GeneratedValue(strategy = GenerationType.IDENTITY)  
    private short id;  
  
    @Column(name = "name", nullable = false)  
    private String name;  
  
    @ManyToOne  
    @JoinColumn(name = "country_code", nullable = false)  
    private Country country;  
  
    public Corporation(){}  
  
}
```

Special annotations and meanings:
- @Table(name = "name") - optional annotation relates class to table in data base. If table name not specified, system relate class with table with identical name
- @Id - essential annotation (only one per class) means that value below is [[sql/Data Base/Schema/Table/Column/Modificators/Primary key|Primary key]]
- @GeneratedValue() - optional annotation get used in conjunction with the @Id annotation to automatically generate unique values.
	Annotation has field "strategy" which provide us with several strategies of value generations:
	- GenerationType.IDENTITY - relies on the database's auto-increment feature
	- GenerationType.SEQUENCE - users a database sequence (Oracle, PostgreSQL), requires a sequence object in the database
	- GenerationType.TABLE - uses a separate table to simulate sequences, works across all databases but has performance overhead
	- GenerationType.AUTO - lets the jpa provider choose the best strategy based on the database
	- GenerationType.UUID - generates a Universally Unique Identifier (UUID) compliant with RFC 4122, Ideal for distributed systems where uniqueness across databases is required.
- @Column(...) - optional annotation relates value below to specific column in table. Has many modificators:
	- name - name of column, as name from @Table, no essential, but if not specified, system relate value with column with identical name
	- nullable - with "false" means that value is [[sql/Data Base/Schema/Table/Column/Modificators/Not null|Not null]], with true means value can be empty or null
	- unique - with "true" means that value is [[Unique]]
- @OneToOne/@ManyToOne/@OneToMany/@ManyToMany(...) - optional annotation specify relations between columns in different tables. Has modificators:
	- mappedBy - defines the "Owner" of the relationship. Prevents JPA from creating two separate FK columns.
	- cascade - 


