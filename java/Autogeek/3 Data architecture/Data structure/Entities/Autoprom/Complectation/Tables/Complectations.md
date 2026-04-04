Table which contains data about [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Complectation|complectations]]

| Field name          | Data type | Unique | Not Null | Default | Description                                                                                                                                |
| ------------------- | --------- | ------ | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| id                  | Serial    | PK     | +        | -       | ID                                                                                                                                         |
| linght_props_id     | JSONB     | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Light_props\|light props]]           |
| anti-theft_props    | JSONB     | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Anti-theft_props\|anti-theft props]] |
| interier_props_id   | JSONB     | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Interier_props\|interier props]]     |
| safety_props_id     | JSONB     | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Safety_props\|safety props]]         |
| multimedia_props_id | JSONB     | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Multimedia_props\|multimedia props]] |
| exterier_props_id   | JSONB     | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Exterier_props\|exterier props]]     |
