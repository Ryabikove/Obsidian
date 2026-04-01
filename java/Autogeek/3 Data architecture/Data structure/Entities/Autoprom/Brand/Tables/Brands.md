Tables which contains data about [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Brand|brands]].

| Имя поля              | Тип данных   | Unique         | Not Null | Default | Описание                                                                                                               |
| --------------------- | ------------ | -------------- | -------- | ------- | ---------------------------------------------------------------------------------------------------------------------- |
| id                    | Small serial | PK             | +        | -       | ID                                                                                                                     |
| short_name            | Varchar(50)  | +              | +        | -       | Short name                                                                                                             |
| full_name             | Varchar(100) | +              | +        | -       | Full name                                                                                                              |
| concern_id            | Small int    | FK one to many | -        | -       | Concern id from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concetn/Tables/Сoncerns\|concerns]]    |
| country_code          | Varchar(3)   | FK one to many | +        | -       | Country code from [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Tables/Countries\|countries]] |
| logo                  | Varchar(255) | +              | -        | -       | Logo brand                                                                                                             |
| capitalization        | Big int      | -              | -        | -       | Capitalization ($)                                                                                                     |
| grows                 | Small int    | -              | -        | -       | Grows of capitalization (%) in 3 year period                                                                           |
| description_n_history | Text         | -              | -        | -       | Philosophy and general concepts of autoconstruction, also brand history                                                |
| produced_auto         | Int          | -              | -        | -       | Cars produced (last year)                                                                                              |
| sold_auto             | Int          | -              | -        | -       | Cars sold (last year)                                                                                                  |
