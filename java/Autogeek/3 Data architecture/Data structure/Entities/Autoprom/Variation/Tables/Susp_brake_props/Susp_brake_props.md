Таблица с характеристиками подвески и тормозной системы.

| Имя поля              | Тип данных | Unique         | Not Null | Default | Описание                                                                                                                                                         |
| --------------------- | ---------- | -------------- | -------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id                    | Serial     | PK             | +        | -       | Идентификатор                                                                                                                                                    |
| front_suspension_type | bytea      | FK one to many | -        | -       | Тип задней подвески из таблицы [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Вариация/Таблицы/Susp_brake_props/Suspension_types\|suspension_types]]   |
| back_suspension_type  | bytea      | FK one to many | -        | -       | Тип передней подвески из таблицы [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Вариация/Таблицы/Susp_brake_props/Suspension_types\|suspension_types]] |
| back_brake_type       | bytea      | FK one to many | -        | -       | Тип задних тормозов из таблицы [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Вариация/Таблицы/Susp_brake_props/Brake_types\|brake_types]]             |
| front_brake_type      | bytea      | FK one to many | -        | -       | Тип передних тормозов из таблицы [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Вариация/Таблицы/Susp_brake_props/Brake_types\|brake_types]]           |
