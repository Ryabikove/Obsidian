Core interface in JPA. It has two resposibilities:
1. Manage the lifecycle of [[JPA/entity/Entity|Entity]];
2. Provide operations for database crud operations;


There are 4 main states of entity:
- *Transient* - temporary object, usually created with [[Java/package/class/New|new]]. It isn't stored in DB and JPA has no info about it.
- *Managed* / *Persistent* - object linked to current session/transaction and will be saved in the end of session or transaction.
- *Detached* - object that is stored in DB and in Java memory, but it must be saved manually into DB, to apply all changes.
- *Removed* - object that will be removed in the end of transaction.

