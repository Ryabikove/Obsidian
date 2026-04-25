Table which contains information about [[Autogeek/4 UX-projecting/Entities/Users/Review/Review|reviews]].

| Field name       | Data type                  | Unique         | Not Null | Default | Description                                                                                                  |
| ---------------- | -------------------------- | -------------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------ |
| id               | Big serial                 | PK             | +        | -       | Id                                                                                                           |
| account_id       | Int                        | FK one to many | +        | -       | Account id from table [[Autogeek/4 UX-projecting/Entities/Users/Account/Tables/Accounts\|accounts]]          |
| generation_id    | Int                        | FK one to many | +        | -       | Generation id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Tables/Generations\|generations]] |
| variation_id     | Int                        | FK one to many | +        | -       | Variation id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Variations\|variations]]     |
| complectation_id | Int                        | FK one to many | -        | -       | id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]]   |
| photos           | Varchar(255)               | +              | -        | -       | link to photos archive                                                                                       |
| description      | Text                       | -              | +        | -       | Description of report                                                                                        |
| creation_date    | Timestamp without timezone | -              | +        | NOW()   | Creation date                                                                                                |
| rating           | JSONB                      | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/JSONB/Rating\|rating]]              |
