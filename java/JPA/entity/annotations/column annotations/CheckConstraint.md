Annotation, which create check constraint for the table. 
Usually used inside attribute uniqueConstraints of [[JPA/entity/annotations/column annotations/Column|Column]] annotations.

Has 3 attributes:
- name - name of constraint (by default - generated automatically);
- constraint - string with native sql expression to be checked;
- options - string which is added to DDL of unique constraint.  (by default - empty);

```
@CheckConstraint(name = "check_name", constraint = "LENGTH(full_name) BETWEEN 3 AND 100")
```