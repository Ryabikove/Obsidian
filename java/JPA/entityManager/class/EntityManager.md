Basic interface, which stores [[JPA/entityManager/class/EntityManager|EntityManager]].

It has several methods:
- find() - retrieve entity by PK;
- persist() - save *new* entity to DB; 
- merge() - update existing entity;
- remove() - delete entity from DB;
- refresh() - reload entity from database;
- detach() - mark entity as [[JPA/entityManager/EntityManager|Detached]];
- clear() - mark all Managed entities as [[JPA/entityManager/EntityManager|Detached]];
- contains() - check if entity is managed;
- flush() - syncronize persistence context with database;