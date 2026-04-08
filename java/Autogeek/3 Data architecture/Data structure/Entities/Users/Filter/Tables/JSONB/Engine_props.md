Jsonb which contains filter engine properties.

| Field name             | Data type | Not Null | Default | Description                                                                                                                                                    |
| ---------------------- | --------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| engine_power           | Smallint  | -        | -       | Engine power (h.p.)                                                                                                                                            |
| engine_type_ids        | bytea     | -        | -       | Engine type from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Engine/Tables/Engine_types\|engine_types]]                                    |
| engine_capacity        | Smallint  | -        | -       | Engine capacity                                                                                                                                                |
| engine_position_id     | bytea     | -        | -       | Engine position type from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Engine/Tables/Engine_positions\|engine_positions]]                   |
| boost_type_id          | bytea     | -        | -       | Boost type from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Engine/Tables/Engine_boost_types\|engine_boost_types]]                         |
| engine_torque          | Smallint  | -        | -       | Torque (N\*m)                                                                                                                                                  |
| cylinders_position_id  | bytea     | -        | -       | Cylinders position from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Engine/Tables/Engine_cylinders_positions\|engine_cylinders_positions]] |
| cylinders_quantity     | bytea     | -        | -       | Cylingers_quantity                                                                                                                                             |
| valves_per_cylinder    | bytea     | -        | -       | Valves per cylinder                                                                                                                                            |
| engine_power_system_id | bytea     | -        | -       | Engine power system type from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Engine/Tables/Engine_power_systems\|engine_power_systems]]       |
| compression_ratio      | bytea     | -        | -       | Compression ratio                                                                                                                                              |
| cylinders_diameter     | Smallint  | -        | -       | Cylinders diameter                                                                                                                                             |
| piston_stroke          | Smallint  | -        | -       | Piston stroke                                                                                                                                                  |
| fuel_type_id           | bytea     | -        | -       | Fuel type from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Engine/Tables/Engine_fuel_types\|engine_fuel_types]]                            |
| co2_emission           | Smallint  | -        | -       | СО2 emission (g/km)                                                                                                                                            |
| review                 | Text      | -        | -       | review                                                                                                                                                         |

Power (hp);
	- Engine type;
	- Boost type;
	- Torque (N\*m);
	- Engine capacity;
	- Engine position;
	- Fuel type;
	- Engine power system type;
	- Compression ratio;
	- СО2 emission (g/km);
	- Cylinders position;
	- Cylingers_quantity;
	- Valves per cylinder;
	- Cylinders diameter;
	- Piston stroke;