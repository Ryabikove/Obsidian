Entity which handles the database (saving and loading data).
Every reposytory is [[Spring/Entitites/Bean|bean]].

Usually all reposytories implemented by [[Spring/packages/org/springframework/data/jpa/reposytory/JpaRepository|JpaRepository]], which add basic methods.
Spring has "Derived Queries" technology. This technology creates whole methods by its name. It looks at parts:
- find - it executes "select" query;
- By - "select" is filtered by value of specific column;
- Column - name of specific column;
- GreaterThan - filtered objects greater than column.

```
@Reposytory
public interface Reposytory extends JpaRepository<Obj, Long> {
	List<Obj> findByColumnGreaterThan(String column); //Custom query
}
```

Created with annotation - [[Spring/Annotations/Entity/Reposytory|Reposytory]].