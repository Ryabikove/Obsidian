Jsonb which contains filter offers properties.

| Field name            | Data type | Not Null | Default | Description                                                                                                                                                                |
| --------------------- | --------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| full_tank_range       | Small int | -        | -       | Full tank range (km)                                                                                                                                                       |
| wheel_orientation_ids | bytea     | -        | -       | Wheel orientation ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Other_props/Wheel_orientation_types\|wheel_orientation_types]] |
| eco_class_ids         | bytea     | -        | -       | Eco class ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Other_props/Eco_classes\|eco_classes]]                                 |
| fuel_consumpt_range   | Small int | -        | -       | Fuel consumption range                                                                                                                                                     |

```
offer_props: [
	full_tank_range: [...],
	wheel_orientation_ids: [...],
	eco_class_ids: [...],
	fuel_consumpt_range [...]
]
```