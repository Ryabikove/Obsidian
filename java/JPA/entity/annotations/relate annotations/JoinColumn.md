Annotation which specifies column settings which is foreign key. 

Has several attributes:
- name - name of column in table, system relates field with column with identical name. (by default - name of field)
- referencedColumnName - name of column in target entity. (By default - primary key of target entity)
- nullable - with "false" means that value is [[sql/Data Base/Schema/Table/Column/Modificators/Not null|Not null]]. (by default `true`);
- unique - with "true" means that value is [[Unique]]. (by default `false`);
- insertable - means that value can be inserted in table (by default `true`);
- updatable - means that inserted value can be updated (by default `true`);
- columnDefinition - sql fragment that is used when generating DDL for the column. (be default empty);
- options - string which is added to DDL (by default - empty);
- table - specify which table stores value (by default - primary table)
- foreignKey - used to specify of control the generation of a foreign key. (By default - [[JPA/entity/annotations/relate annotations/ForeignKey|PROVIDER_DEFAULT]])
- check - specify check constraints for column (by default - empty). Creates with annotation [[JPA/entity/annotations/column annotations/CheckConstraint|CheckConstraint]];
- comment - comment to table (by default - empty);

```
@ManyToOne
@JoinColumn(name = "country_code",
	referencedColumnName = "code",
	unique = false,
	nullable = false,
	nullable = false,
	)
class Country country;
```