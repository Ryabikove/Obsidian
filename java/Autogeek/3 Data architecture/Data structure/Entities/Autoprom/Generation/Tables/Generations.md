Table which contains data about [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Generation/Generation|generations]]

| Field name           | Data type    | Unique         | Not Null | Default | Description                                                                                                                          |
| -------------------- | ------------ | -------------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| id                   | Serial       | PK             | +        | -       | ID                                                                                                                                   |
| full_name            | Varchar(100) | +              | +        | -       | Full name                                                                                                                            |
| photos               | Varchar(255) | +              | -        | -       | link to photos archive                                                                                                               |
| brand_id             | Smallint     | FK one to many | +        | -       | brand which generation belongs to from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] |
| model_id             | Int          | FK one to many | +        | -       | model which generation belongs to from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Tables/Models\|models]] |
| year_start           | Smallint     | -              | -        | -       | start of construction                                                                                                                |
| year_stop            | Smallint     | -              | -        | -       | end of construction                                                                                                                  |
| produced_auto        | Int          | -              | -        | -       | how many were produced                                                                                                               |
| sold_auto            | Int          | -              | -        | -       | how many were sold                                                                                                                   |
| description_n_review | Text         | -              | -        | -       | Description + review                                                                                                                 |
| prices_range         | Int          | -              | -        | -       | Prices range from [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Offers\|offers]]                         |

