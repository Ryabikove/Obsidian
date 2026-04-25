Table which contains data about [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Generation|generations]]

| Field name           | Data type    | Unique         | Not Null | Default | Description                                                                                                       |
| -------------------- | ------------ | -------------- | -------- | ------- | ----------------------------------------------------------------------------------------------------------------- |
| id                   | Serial       | PK             | +        | -       | ID                                                                                                                |
| full_name            | Varchar(100) | +              | +        | -       | Full name                                                                                                         |
| photos               | Varchar(255) | +              | -        | -       | link to photos archive                                                                                            |
| model_id             | Int          | FK one to many | +        | -       | model which generation belongs to from [[Autogeek/4 UX-projecting/Entities/Autoprom/Model/Tables/Models\|models]] |
| car_class            | Varchar(255) | -              | -        | -       | car_class_id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Tables/enums/CarClass\|car_classes]]       |
| year_start           | Smallint     | -              | -        | -       | start of construction                                                                                             |
| year_stop            | Smallint     | -              | -        | -       | end of construction                                                                                               |
| produced_auto        | Int          | -              | -        | -       | how many were produced                                                                                            |
| sold_auto            | Int          | -              | -        | -       | how many were sold                                                                                                |
| description_n_review | Text         | -              | -        | -       | Description + review                                                                                              |
| price_max            | Int          | -              | -        | -       | Prices max from [[Autogeek/4 UX-projecting/Entities/Users/Offer/Tables/Offers\|offers]]                           |
| price_min            | Int          | -              | -        | -       | Prices min from [[Autogeek/4 UX-projecting/Entities/Users/Offer/Tables/Offers\|offers]]                           |

