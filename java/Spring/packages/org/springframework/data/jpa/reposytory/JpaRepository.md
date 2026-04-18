Interface, which allows us to add methods with JPA logic in custom classes.
Usually used in [[Spring/Entitites/Reposytory|reposytory]]

Has methods:
- `save()` - saves entity in DB;
- `findAll()` - get all entities from DB table;
- `deleteById()` - delete entity by id from DB;
- `findById()` - find entity by ID;
- `count()` - count number of strings in table.