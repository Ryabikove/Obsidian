Annotation which specifies relations between columns in different tables.

Has several attributes:
- mappedBy - defines the "Owner" of the relationship. Prevents JPA from creating two separate FK columns.
- cascade - 

```
@OneToMany  
private Country country;
```