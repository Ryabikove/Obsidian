Annotation map [[Java/package/class/Field|field]] below to specific column in table.

Optional annotation.

Has several attributes:
- name - name of column in table, system relates field with column with identical name. (by default - name of field)
- nullable - with "false" means that value is [[sql/Data Base/Schema/Table/Column/Modificators/Not null|Not null]]. (by default `true`);
- unique - with "true" means that value is [[Unique]]. (by default `false`);
- insertable - means that value can be inserted in table (by default `true`);
- updatable - means that inserted value can be updated (by default `true`);
- columnDefinition - sql fragment that is used when generating DDL for the column. (be default empty);
- options - string which is added to DDL (by default - empty);
- table - specify which table stores value (by default - primary table)
- length - column length. Applied only to parametrized by length types like varchar or varbinary (by default 255);
- precision - precision for a column of decimal or numeric type (or similar) (by default 0 - means that precision specified by SQL provider);
- scale - scale for a column of decimal or numeric type (or similar) (by default 0 - means that precision specified by SQL provider);
- secondPrecision - precision for a column of time or timestamp type (or similar) (by default -1 - means hat fractional seconds should not be stored in a time column, or that the maximum number of digits supported by the database and JDBC should be stored in a timestamp column );
- check - specify check constraints for column (by default - empty). Creates with annotation [[JPA/entity/annotations/column annotations/CheckConstraint|CheckConstraint]];
- comment - comment to table (by default - empty);

```
@Column(name = "name",
	nullable = false,
	unique = true,
	insertable = false,
	updatable = false,
	columnDefinition = "TEXT",
	table = "corporations",
	length = 100,
	check = {
		@CheckConstraint(name = "check_name", constraint = "LENGHT(name) BETWEEN 3 AND 30")
	},
	comment = "It is full name of corporation"
)  
private String name;  
```