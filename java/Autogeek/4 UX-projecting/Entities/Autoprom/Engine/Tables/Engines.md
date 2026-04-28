Table which containc properties of [[Autogeek/4 UX-projecting/Entities/Autoprom/Engine/Engine|engines]].

| Field name          | Data type    | Unique         | Not Null | Default | Description                                                                                                                            |
| ------------------- | ------------ | -------------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| id                  | Serial       | PK             | +        | -       | ID                                                                                                                                     |
| full_name           | Varchar(250) | +              | +        | -       | Full name                                                                                                                              |
| photos              | Varchar(255) | +              | -        | -       | Link to photos archive                                                                                                                 |
| engine_parent_id    | Int          | FK one to many | -        | -       | Engine parent id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Engine/Tables/Engines\|engines]]                                    |
| engine_capacity     | Smallint     | -              | -        | -       | Engine capacity                                                                                                                        |
| engine_type         | Varchar(255) | -              | -        | -       | Engine type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Engine/Tables/enums/EngineType\|EngineTypes]]                            |
| engine_power_system | Varchar(255) | -              | -        | -       | Engine power system type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Engine/Tables/enums/EnginePowerSystem\|EnginePowerSystems]] |
| engine_power        | Smallint     | -              | -        | -       | Engine power (h.p.)                                                                                                                    |
| engine_torque       | Smallint     | -              | -        | -       | Torque (N\*m)                                                                                                                          |
| cylinders_position  | Varchar(255) | -              | -        | -       | Cylinders position from [[Autogeek/4 UX-projecting/Entities/Autoprom/Engine/Tables/enums/CylindersPosition\|CylindersPositions]]       |
| cylinders_quantity  | bytea        | -              | -        | -       | Cylingers_quantity                                                                                                                     |
| valves_per_cylinder | bytea        | -              | -        | -       | Valves per cylinder                                                                                                                    |
| compression_ratio   | bytea        | -              | -        | -       | Compression ratio                                                                                                                      |
| cylinders_diameter  | Smallint     | -              | -        | -       | Cylinders diameter                                                                                                                     |
| piston_stroke       | Smallint     | -              | -        | -       | Piston stroke                                                                                                                          |
| fuel_type           | Varchar(255) | -              | -        | -       | Fuel type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Engine/Tables/enums/FuelType\|FuelTypes]]                                  |
| co2_emission        | Smallint     | -              | -        | -       | СО2 emission (g/km)                                                                                                                    |
| review              | Text         | -              | -        | -       | review                                                                                                                                 |
*Relations*:

| Mapped entity                                                                         | Column           | Relation type | Fetch type | Cascade | Orhpan removal |
| ------------------------------------------------------------------------------------- | ---------------- | ------------- | ---------- | ------- | -------------- |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Engine/Tables/Engines\|Engine]]          | engine_parent_id | Many to one   | LAZY       | REFRESH | -              |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Engine/Tables/Engines\|Engine]]          | -                | One to many   | LAZY       | ALL     | true           |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Variations\|Variation]] | -                | One to many   | LAZY       | ALL     | true           |
