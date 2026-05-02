Table which contains data about [[Autogeek/4 UX-projecting/Entities/Autoprom/Complectation/Complectation|complectations]]

| Field name       | Data type    | Unique         | Not Null | Default | Description                                                                                                             |
| ---------------- | ------------ | -------------- | -------- | ------- | ----------------------------------------------------------------------------------------------------------------------- |
| id               | Serial       | PK             | +        | -       | ID                                                                                                                      |
| full_name        | Varchar(100) | -              | +        | -       | Name of complectation                                                                                                   |
| generation_id    | Int          | FK one to many | +        | -       | id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Tables/Generations\|generations]]                       |
| linght_props     | JSONB        | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Complectation/Tables/JSONB/Light_props\|light props]]           |
| antitheft_props  | JSONB        | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Complectation/Tables/JSONB/Antitheft_props\|antitheft props]]   |
| interior_props   | JSONB        | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Complectation/Tables/JSONB/Interior_props\|interior props]]     |
| safety_props     | JSONB        | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Complectation/Tables/JSONB/Safety_props\|safety props]]         |
| multimedia_props | JSONB        | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Complectation/Tables/JSONB/Multimedia_props\|multimedia props]] |
| exterior_props   | JSONB        | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Complectation/Tables/JSONB/Exterior_props\|exterior props]]     |
*Relations*:

| Mapped table                                                                              | Column        | Relation type | Fetch type | Cascade | Orhpan removal | Optional |
| ----------------------------------------------------------------------------------------- | ------------- | ------------- | ---------- | ------- | -------------- | -------- |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Tables/Generations\|Generations]] | generation_id | Many to one   | LAZY       | REFRESH | -              | false    |
| [[Autogeek/4 UX-projecting/Entities/Users/Report/Tables/Reports\|Reports]]                | -             | One to many   | LAZY       | ALL     | true           | -        |
