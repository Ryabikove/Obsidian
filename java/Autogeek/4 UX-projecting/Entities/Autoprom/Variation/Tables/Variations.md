Table which contains data about [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Variation|variations]]

| Имя поля             | Тип данных   | Unique         | Not Null | Default | Описание                                                                                                                |
| -------------------- | ------------ | -------------- | -------- | ------- | ----------------------------------------------------------------------------------------------------------------------- |
| id                   | Serial       | PK             | +        | -       | ID                                                                                                                      |
| full_name            | Varchar(100) | +              | +        | -       | Full name                                                                                                               |
| generation_id        | Int          | FK one to many | +        | -       | Generation id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Tables/Generations\|generations]]            |
| class                | Bytea        | -              | -        | -       | Car class                                                                                                               |
| body_type            | Bytea        | FK one to many | -        | -       | Body type id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Body_types\|body_types]]                |
| drive_type_id        | Bytea        | FK one to many | -        | -       | Drive type id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Other_props/Drive_types\|drive_types]] |
| engine_id            | Int          | FK one to many | -        | -       | Engine id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Engine/Tables/Engines\|engines]]                            |
| gearbox_id           | Int          | FK one to many | -        | -       | Gearbox id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Gearbox/Tables/Gearboxes\|gearboxes]]                      |
| rating               | JSONB        | -              | -        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/JSONB/Rating\|rating]]                         |
| body_props           | JSONB        | -              | +        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/JSONB/Body_props\|body props]]                 |
| susp_brake_props     | JSONB        | -              | +        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/JSONB/Susp_brake_props\|susp brake props]]     |
| other_props          | JSONB        | -              | +        | -       | Jsonb with [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/JSONB/Other_props\|other props]]               |
| description_n_review | Text         | -              | -        | -       | Description and review                                                                                                  |
| acl_to_100           | bytea        | -              | -        | -       | Acceleration to 100 (s/10)                                                                                              |
| fuel_per_100         | bytea        | -              | -        | -       | Fuel consumption per 100 km (l);                                                                                        |
