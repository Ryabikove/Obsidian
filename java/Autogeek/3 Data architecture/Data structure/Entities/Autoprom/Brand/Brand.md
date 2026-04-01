Entity which represent an auto brand.

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands|brands]].

*Full presentation:*

| Description                                                                                                              | Field name                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                                                | full_name                                                                                                                           |
| Logo                                                                                                                     | logo                                                                                                                                |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concetn/Concern\|Concern]] name-link                     | name из [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Концерн/Таблицы/Сoncerns\|concerns]] по concern_id        |
| Ссылка-название на [[Autogeek/3 Data architecture/Структура данных/Сущности/General/Country/Country\|страну]]            | full_name из [[Autogeek/3 Data architecture/Структура данных/Сущности/General/Country/Tables/Countries\|countries]] по country_code |
| Список ссылок-названий [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Модель/Модель\|моделей]] бренда | name из [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Модель/Таблицы/Models\|models]] по id                     |
| Капитализация                                                                                                            | capitalization                                                                                                                      |
| Темпы роста                                                                                                              | grows                                                                                                                               |
| Описание концепции + общие принципы машиностроения. Информация об истории бренда                                         | description_n_history                                                                                                               |
| Список стран, где производят автомобили                                                                                  | #TODO подумать над реализацией                                                                                                      |
| Кол-во продаваемых единиц авто                                                                                           | produced_auto                                                                                                                       |
| Кол-во производимых единиц                                                                                               | sold_auto                                                                                                                           |
*Краткое представление:*

| Description                                                                                                             | Field name                                                                                                                          |
| ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Краткое название                                                                                                        | short_name                                                                                                                          |
| Ссылка-название [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Концерн/Концерн\|концерна-владельца]] | name из [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Концерн/Таблицы/Сoncerns\|concerns]] по concern_id        |
| Логотип                                                                                                                 | logo                                                                                                                                |
| Ссылка-название на [[Autogeek/3 Data architecture/Структура данных/Сущности/General/Country/Country\|страну]]           | full_name из [[Autogeek/3 Data architecture/Структура данных/Сущности/General/Country/Tables/Countries\|countries]] по country_code |
[[Autogeek/3 Data architecture/Карты/Модули/Дополнительные/Список сущностей|Полное и краткое представления]]

Может быть представлена в виде [[Autogeek/3 Data architecture/Карты/Модули/Дополнительные/Список сущностей|списка сущностей]]