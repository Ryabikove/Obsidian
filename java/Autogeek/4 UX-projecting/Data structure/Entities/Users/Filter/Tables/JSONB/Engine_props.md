Jsonb which contains filter engine properties.

| Field name                | Data type | Not Null | Default | Description                                                                                                                                                    |
| ------------------------- | --------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| power_range               | Smallint  | -        | -       | Engine power (h.p.)                                                                                                                                            |
| engine_type_ids           | bytea     | -        | -       | Engine type from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Engine/Tables/Engine_types\|engine_types]]                                    |
| boost_type_ids            | bytea     | -        | -       | Boost type from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Engine/Tables/Engine_boost_types\|engine_boost_types]]                         |
| torque                    | Smallint  | -        | -       | Torque (N\*m)                                                                                                                                                  |
| engine_capacity_range     | Smallint  | -        | -       | Engine capacity                                                                                                                                                |
| engine_position_ids       | bytea     | -        | -       | Engine position type from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Engine/Tables/Engine_positions\|engine_positions]]                   |
| fuel_type_ids             | bytea     | -        | -       | Fuel type from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Engine/Tables/Engine_fuel_types\|engine_fuel_types]]                            |
| engine_power_system_ids   | bytea     | -        | -       | Engine power system type from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Engine/Tables/Engine_power_systems\|engine_power_systems]]       |
| compression_ratio_range   | bytea     | -        | -       | Compression ratio                                                                                                                                              |
| co2_emission_range        | Smallint  | -        | -       | СО2 emission (g/km)                                                                                                                                            |
| cylinders_position_ids    | bytea     | -        | -       | Cylinders position from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Engine/Tables/Engine_cylinders_positions\|engine_cylinders_positions]] |
| cylinders_quantity_range  | bytea     | -        | -       | Cylingers_quantity                                                                                                                                             |
| valves_per_cylinder_range | bytea     | -        | -       | Valves per cylinder                                                                                                                                            |
| cylinders_diameter_range  | Smallint  | -        | -       | Cylinders diameter                                                                                                                                             |
| piston_stroke_range       | Smallint  | -        | -       | Piston stroke                                                                                                                                                  |

```
engine_props: [
	power_range: [...],
	engine_type_ids: [...],
	boost_types: [...],
	torque: [...],
	engine_capacity_range: [...],
	engine_position_ids: [...],
	fuel_type_ids: [...],
	engine_power_system_ids: [...],
	compression_ratio_range: [...],
	co2_emission: [...],
	cylinders_position_ids: [...],
	cylingers_quantity_range: [...],
	valves_per_cylinder_range: [...],
	cylinders_diameter_range: [...],
	piston_stroke_range: [...]
]
```
