Table which contains data about [[Autogeek/3 Data architecture/Структура данных/Сущности/General/City/City|cities]].

| Имя поля     | Тип данных   | Unique         | Not Null | Default | Описание                                                                                                                 |
| ------------ | ------------ | -------------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------ |
| id           | Serial       | PK             | +        | -       | ID                                                                                                                       |
| country_code | Varchar(3)   | FK one ot many | +        | -       | Country code from [[Autogeek/3 Data architecture/Структура данных/Сущности/General/Country/Tables/Countries\|countries]] |
| full_name    | Varchar(200) | -              | +        | -       | Full name                                                                                                                |
