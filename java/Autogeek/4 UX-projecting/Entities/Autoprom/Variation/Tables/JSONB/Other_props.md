Jsonb which contains other properties.

| Field name           | Data type | Not Null | Default | Description                                                                                                                                                                 |
| -------------------- | --------- | -------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| max_range            | Smallint  | -        | -       | Max range for full tank                                                                                                                                                     |
| wheel_orientation_id | Вytea     | -        | -       | Wheel orientation type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Other_props/Wheel_orientation_types\|wheel_orientation_types]] |
| eco_class_id         | Вytea     | -        |         | Eco class id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Other_props/Eco_classes\|eco_classes]]                                   |
| 0_to_100             | Bytea     | -        | -       | acceleration from 0 to 100 (10 ms)                                                                                                                                          |
| fuel_consumption     | Bytea     | -        | -       | Fuel consumption on 100 km (mixed)                                                                                                                                          |

```
other_props: [
	max_range: ...,
	wheel_orientation_id: ...,
	eco_class_id: ...,
	0_to_100: ...,
	fuel_consumption: ...
]
```