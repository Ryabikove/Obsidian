Таблица, содержащая характеристики кузова.

| Имя поля           | Тип данных | Unique         | Not Null | Default | Описание                                                                                                                                  |
| ------------------ | ---------- | -------------- | -------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| id                 | Serial     | PK             | +        | -       | Идентификатор                                                                                                                             |
| body_type          | Bytea      | FK one to many | -        | -       | Тип кузова из таблицы [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Вариация/Таблицы/Body_props/Body_types\|body_types]] |
| body_length        | Smallint   | -              | -        | -       | Длина кузова (мм)                                                                                                                         |
| body_width         | Smallint   | -              | -        | -       | Ширина кузова (мм)                                                                                                                        |
| body_heigth        | Smallint   | -              | -        | -       | Высота кузова (мм)                                                                                                                        |
| wheel_base         | Smallint   | -              | -        | -       | Колесная база (мм)                                                                                                                        |
| front_track        | Smallint   | -              | -        | -       | Передняя колея (мм)                                                                                                                       |
| back_track         | Smallint   | -              | -        | -       | Задняя колея (мм)                                                                                                                         |
| doors_number       | Bytea      | -              | -        | -       | Кол-во дверей                                                                                                                             |
| seats_number       | Bytea      | -              | -        | -       | Кол-во сидений                                                                                                                            |
| empty_weight       | Smallint   | -              | -        | -       | Снаряженная масса (кг)                                                                                                                    |
| full_weight        | Smallint   | -              | -        | -       | Полная масса (кг)                                                                                                                         |
| min_trunk_capacity | Smallint   | -              | -        | -       | Минимальный объем багажника (л)                                                                                                           |
| max_trunk_capacity | Smallint   | -              | -        | -       | Максимальный объем багажника (л)                                                                                                          |
| tank_capacity      | Smallint   | -              | -        | -       | Объем топливного бака (л)                                                                                                                 |


