Table with data about [[Autogeek/3 Data architecture/Data structure/Entities/Users/Filter/Filter|filters]].

| Field name           | Data type  | Unique         | Not Null | Default | Description                                                                                                                            |
| -------------------- | ---------- | -------------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| id                   | Big Serial | PK             | +        | -       | ID                                                                                                                                     |
| account_id           | Int        | FK one to many | +        | -       | Id from [[Autogeek/3 Data architecture/Data structure/Entities/Users/Account/Tables/Accounts\|accounts]]                               |
| full_name            | JSONB      | -              | +        | -       | Full name                                                                                                                              |
| primary_props        | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Users/Filter/Tables/JSONB/Primary_props\|primary_props]]             |
| complectation_props  | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Users/Filter/Tables/JSONB/Complectation_props\|complectation_props]] |
| offer_props          | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Users/Filter/Tables/JSONB/Offer_props\|offer_props]]                 |
| body_props           | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Users/Filter/Tables/JSONB/Body_props\|body_props]]                   |
| engine_props         | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Users/Filter/Tables/JSONB/Engine_props\|engine_props]]               |
| gearbox_props        | JSONB      | -              | -        | -       | Jsonb with Gearbox properties                                                                                                          |
| brake_and_susp_props | JSONB      | -              | -        | -       | Jsonb with Brake and suspencion properties                                                                                             |
| other_props          | JSONB      | -              | -        | -       | Jsonb with Other properties                                                                                                            |
