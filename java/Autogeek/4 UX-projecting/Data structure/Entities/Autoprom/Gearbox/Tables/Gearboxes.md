Tables which contains data about [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Gearbox/Gearbox|gearboxes]]

| Field name        | Data type    | Unique         | Not Null | Default | Description                                                                                                                     |
| ----------------- | ------------ | -------------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------------- |
| id                | Serial       | PK             | +        | -       | ID                                                                                                                              |
| full_name         | Varchar(250) | +              | +        | -       | Full name                                                                                                                       |
| photos            | Varchar(255) | +              | -        | -       | link to photos archive                                                                                                          |
| gearbox_parent_id | Int          | FK one to many | -        | -       | parent gearbox from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Gearbox/Tables/Gearboxes\|gearboxes]]       |
| gearbox_type      | Bytea        | FK one to many | -        | -       | gearbox type from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Gearbox/Tables/Gearbox_types\|gearbox_types]] |
| gear_quantity     | Bytea        | -              | -        | -       | gear quantity                                                                                                                   |
| review            | Text         | -              | -        | -       | review                                                                                                                          |
