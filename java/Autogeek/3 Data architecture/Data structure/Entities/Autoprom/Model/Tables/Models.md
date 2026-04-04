Tables which contains data about [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Model|models]].

| Field name            | Data type    | Unique         | Not Null | Default | Description                                                                                                    |
| --------------------- | ------------ | -------------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------- |
| id                    | Serial       | PK             | +        | -       | ID                                                                                                             |
| full_name             | Varchar(100) | +              | +        | -       | Full name                                                                                                      |
| photos                | Varchar(255) | +              | -        | -       | link to photos archive                                                                                         |
| brand_id              | Small int    | FK one to many | +        | -       | Brand-owner from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] |
| description_n_history | Text         | -              | -        | -       | Description and history                                                                                        |
