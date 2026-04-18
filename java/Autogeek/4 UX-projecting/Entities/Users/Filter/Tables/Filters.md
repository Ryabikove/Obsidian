Table with data about [[Autogeek/4 UX-projecting/Entities/Users/Filter/Filter|filters]].

| Field name          | Data type  | Unique         | Not Null | Default | Description                                                                                                                            |
| ------------------- | ---------- | -------------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| id                  | Big Serial | PK             | +        | -       | ID                                                                                                                                     |
| account_id          | Int        | FK one to many | +        | -       | Id from [[Autogeek/4 UX-projecting/Entities/Users/Account/Tables/Accounts\|accounts]]                               |
| full_name           | JSONB      | -              | +        | -       | Full name                                                                                                                              |
| primary_props       | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Filter/Tables/JSONB/Primary_props\|primary_props]]             |
| complectation_props | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Filter/Tables/JSONB/Complectation_props\|complectation_props]] |
| offer_props         | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Filter/Tables/JSONB/Offer_props\|offer_props]]                 |
| body_props          | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Filter/Tables/JSONB/Body_props\|body_props]]                   |
| engine_props        | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Filter/Tables/JSONB/Engine_props\|engine_props]]               |
| gearbox_props       | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Filter/Tables/JSONB/Gearbox_props\|gearbox_props]]             |
| brake_n_susp_props  | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Filter/Tables/JSONB/Brake_n_susp_props\|brake_n_susp_props]]   |
| other_props         | JSONB      | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Filter/Tables/JSONB/Other_props\|other_props]]                 |
