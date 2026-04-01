Седьмой раздел обучения языку java. Является продолжением третьего раздела.
Представляет из себя технологию Java Persistenc Api - представление строки таблицы из БД в виде класса, а колонок строки в виде атрибутов класса.

Hibernate - наиболее популярный фреймворк, реализующий технологию JPA

Рекомендуемые курсы:
- https://youtube.com/playlist?list=PL8X2nqRlWfabN7rXPD7KDfXd8jFhAmkTL&si=gw8jWokYe7oHjymR
- https://youtube.com/playlist?list=PL8X2nqRlWfabWFN81Zi4vl30cZsdyxt6e&si=ZO6oTWTa70kOR6cF
Статьи:
- https://javarush.com/groups/posts/2259-jpa--znakomstvo-s-tekhnologiey
- https://www.baeldung.com/learn-jpa-hibernate

JPA - Java Persistence API - спецификация, позволяющая нам связывать java-объекты с таблицами в реляционных базах данных.
Такой процесс называется ORM (Object-Relational Mapping). Вместо того, чтобы вручную писать сложные sql-запросы для каждой операции, мы работаем с обычными java классами, а все остальное преобразуется автоматически.

JPA состоит из 3 составляющих:
- [[Study/7 jpa & hibernate/Entity|Entity]] (Сущность) - обычный java класс, помеченный специальными аннотациями, который JPA воспринимает как схему таблицы.
- [[Study/7 jpa & hibernate/EntityManager|EntityManager]] - основной интерфейс, который управляет жизненным циклом объектов (сохраняет, обновляет, ищет и удаляет их)
- [[Study/7 jpa & hibernate/Persistence Provider|Persistence Provider]] - реализация стандарта. JPA - это лишь референс или правила, а реализация правил происходит в библиотеке (например Hibernate)