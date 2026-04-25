Annotation, which make indexes for this table.
Usually used inside attribute uniqueConstraints of [[JPA/entity/annotations/table annotations/Table|Table]] annotations.

Has 3 attributes:
- name - name of index (by default - generated automatically);
- columnList - list of columns, which combination will be indexed;
- unique - prevents duplicate emails;
- options - string which is added to DDL.  (by default - empty);

```
@Index(name = "uk_email", columnList = "email, id, number")
```