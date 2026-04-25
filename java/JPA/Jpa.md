JPA - Java Persistence API - technolody which maps java classes to tables in data base.

Process of relating is called ORM (Object-Relational Mapping). Instead of writing sql requests for every operation, we work with common java classes.

JPA has 3 main objects:
- [[JPA/entity/Entity|Entity]] - common java class with special annotation [[JPA/entity/annotations/Entity|@Entity]]. JPA works with this class as with table in DB.
- [[JPA/entityManager/EntityManager|EntityManager]] - основной интерфейс, который управляет жизненным циклом объектов (сохраняет, обновляет, ищет и удаляет их)
- [[JPA/persistence provider/Persistence Provider|Persistence Provider]] - реализация стандарта. JPA - это лишь референс или правила, а реализация правил происходит в библиотеке (например Hibernate)