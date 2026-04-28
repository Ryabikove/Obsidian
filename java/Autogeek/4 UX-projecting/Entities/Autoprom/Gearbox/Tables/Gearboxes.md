Tables which contains data about [[Autogeek/4 UX-projecting/Entities/Autoprom/Gearbox/Gearbox|gearboxes]]

| Field name        | Data type    | Unique         | Not Null | Default | Description                                                                                                     |
| ----------------- | ------------ | -------------- | -------- | ------- | --------------------------------------------------------------------------------------------------------------- |
| id                | Serial       | PK             | +        | -       | ID                                                                                                              |
| full_name         | Varchar(250) | +              | +        | -       | Full name                                                                                                       |
| photos            | Varchar(255) | +              | -        | -       | link to photos archive                                                                                          |
| gearbox_parent_id | Int          | FK one to many | -        | -       | parent gearbox from [[Autogeek/4 UX-projecting/Entities/Autoprom/Gearbox/Tables/Gearboxes\|gearboxes]]          |
| gearbox_type      | Varchar(255) | -              | -        | -       | gearbox type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Gearbox/Tables/enums/GearboxType\|GearboxTypes]] |
| gear_quantity     | Bytea        | -              | -        | -       | gear quantity                                                                                                   |
| review            | Text         | -              | -        | -       | review                                                                                                          |

*Relations*:

| Mapped entity                                                                         | Column            | Relation type | Fetch type | Cascade | Orhpan removal |
| ------------------------------------------------------------------------------------- | ----------------- | ------------- | ---------- | ------- | -------------- |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Gearbox/Tables/Gearboxes\|Gearbox]]      | gearbox_parent_id | Many to one   | LAZY       | REFRESH | -              |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Gearbox/Tables/Gearboxes\|Gearbox]]      | -                 | One to many   | LAZY       | ALL     | true           |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Variations\|Variation]] | -                 | One to many   | LAZY       | ALL     | true           |
