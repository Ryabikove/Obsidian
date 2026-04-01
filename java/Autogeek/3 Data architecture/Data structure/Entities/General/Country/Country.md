Entity which represent country in general

*Table in DB* - [[Autogeek/3 Data architecture/Структура данных/Сущности/General/Country/Tables/Countries|countries]].
*Full presentation:*

| Description                                                                                                      | Field name                                                                                                         |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| Full name                                                                                                        | full_name                                                                                                          |
| Image of flag                                                                                                    | flag                                                                                                               |
| List of [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Концерн/Концерн\|concerns]] name-links | name from [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Концерн/Концерн\|concern]] on iso_code |
| List of [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Brand/Brand\|brands]] name-links       | name from [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Brand/Brand\|brands]] on iso_code      |
| Information about autoconstruction in country:<br>- Which brands and models are constructed<br>- How many        | #TODO think about realisation                                                                                      |
*Short presentation:*

| Description   | Field name |
| ------------- | ---------- |
| Full name     | full_name  |
| Image of flag | flag       |

[[Autogeek/3 Data architecture/Карты/Модули/Дополнительные/Список сущностей|Full and short presentations]].

Can be shown as [[Autogeek/3 Data architecture/Карты/Модули/Дополнительные/Список сущностей|entities list]].