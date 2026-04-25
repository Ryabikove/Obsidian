Annotation, which specify [[JPA/entity/Entity|Entity]] table settings.

Optional annotation. If table name not specified, system relate class with table with identical name.

Has several attributes:
- name - name of table in DB (by default name of class);
- schema - name of schema in DB (by default - default schema);
- catalog - name of catalog in DB (by default - default catalog);
- options - extra options which added to DDL while create table (by default - empty);
- comment - comment to table (by default - empty);
- indexes - indexes for table (by default - empty). Created with annotation [[JPA/entity/annotations/table annotations/Index|Index]];
- uniqueConstraint - [[sql/Data Base/Schema/Table/Column/Modificators/Unique|unique]] constraint for table, applied to constraint in [[JPA/entity/annotations/column annotations/Column|Column]], [[JPA/entity/annotations/relate annotations/JoinColumn|JoinColumn]] and primary key mapping (by default - empty). Created with annotation [[JPA/entity/annotations/table annotations/UniqueConstraint|UniqueConstraint]].

```
@Entity
@Table(name = "corporations",
schema = "public",
catalog = "tables",
comment = "This is table",
options = "",
indexes = {
	@Index(name = "idx_corporation_name", columnList = "full_name")
	},
uniqueConstraint = {
	@UniqueConstraint(name = "uk_email", columnNames = {"email"})
	}
) 
class Corporation{}
```