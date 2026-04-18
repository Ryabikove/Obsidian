Table which contains information about [[Autogeek/4 UX-projecting/Entities/Users/Article/Article|articles]].

| Field name    | Data type                  | Unique | Not Null | Default | Description                                                                                                                 |
| ------------- | -------------------------- | ------ | -------- | ------- | --------------------------------------------------------------------------------------------------------------------------- |
| id            | Big serial                 | PK     | +        | -       | Id                                                                                                                          |
| photos        | Varchar(255)               | +      | -        | -       | link to photos archive                                                                                                      |
| description   | Text                       | -      | +        | -       | Description of report                                                                                                       |
| creation_date | Timestamp without timezone | -      | +        | NOW()   | Creation date                                                                                                               |
| rating        | JSONB                      | -      | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/JSONB/Rating\|rating]]          |
| entities_list | JSONB                      | -      | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Article/Tables/JSONB/Entity_list\|entities_list]] |
