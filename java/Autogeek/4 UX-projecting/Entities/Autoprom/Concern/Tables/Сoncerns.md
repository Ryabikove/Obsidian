Table which contains data about [[Autogeek/4 UX-projecting/Entities/Autoprom/Concern/Concern|concerns]].

| Field name            | Data type    | Unique         | Not Null | Default | Description                                                                                     |
| --------------------- | ------------ | -------------- | -------- | ------- | ----------------------------------------------------------------------------------------------- |
| id                    | Small serial | PK             | +        | -       | ID                                                                                              |
| short_name            | Varchar(50)  | +              | +        | -       | Short name                                                                                      |
| full_name             | Varchar(100) | +              | +        | -       | Full name                                                                                       |
| logo                  | Varchar(255) | +              | -        | -       | Concens logo                                                                                    |
| country_code          | Varchar(3)   | FK one to many | +        | -       | iso_code from [[Autogeek/4 UX-projecting/Entities/General/Country/Tables/Countries\|countries]] |
| main_brand_id         | Int          | FK one to one  | +        | -       | brand_id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Brand/Tables/Brands\|brands]]        |
| capitalization        | Small int    | -              | -        | -       | Capitalization (bil $)                                                                          |
| grows                 | Bytea        | -              | -        | -       | Grows of capitalization (%) in 3 year period                                                    |
| description_n_history | Text         | -              | -        | -       | Concern's description and history                                                               |
