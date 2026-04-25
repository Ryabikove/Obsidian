Annotation, which mark fields in table as [[sql/Data Base/Schema/Table/Column/Modificators/Unique|unique]].
Usually used inside attribute uniqueConstraints of [[JPA/entity/annotations/table annotations/Table|Table]] annotations.

Has 3 attributes:
- name - name of constraint (by default - generated automatically);
- columnNames - list of columns, which combination musts be unique;
- options - string which is added to DDL of unique constraint.  (by default - empty);

```
@UniqueConstraint(name = "uk_email", columnNames = {"email"})
```