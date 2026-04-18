Tables which contains data about [[Autogeek/4 UX-projecting/Entities/Autoprom/Brand/Brand|brands]].

| Field name            | Data type    | Unique         | Not Null | Default | Description                                                                                         |
| --------------------- | ------------ | -------------- | -------- | ------- | --------------------------------------------------------------------------------------------------- |
| id                    | Small serial | PK             | +        | -       | ID                                                                                                  |
| short_name            | Varchar(50)  | +              | +        | -       | Short name                                                                                          |
| full_name             | Varchar(100) | +              | +        | -       | Full name                                                                                           |
| concern_id            | Small int    | FK one to many | -        | -       | Concern id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Concern/Tables/Сoncerns\|concerns]]    |
| country_code          | Varchar(3)   | FK one to many | +        | -       | Country code from [[Autogeek/4 UX-projecting/Entities/General/Country/Tables/Countries\|countries]] |
| logo                  | Varchar(255) | +              | -        | -       | Logo brand                                                                                          |
| capitalization        | Int          | -              | -        | -       | Capitalization (mil $)                                                                              |
| growth                | Bytea        | -              | -        | -       | Grows of capitalization (%) in 3 year period                                                        |
| description_n_history | Text         | -              | -        | -       | Brand's description and history                                                                     |
| produced_auto         | Int          | -              | -        | -       | Cars produced (last year)                                                                           |
| sold_auto             | Int          | -              | -        | -       | Cars sold (last year)                                                                               |
