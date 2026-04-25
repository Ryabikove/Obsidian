Jsonb which contains other properties.

| Field name        | Data type    | Not Null | Default | Description                                                                                                                                  |
| ----------------- | ------------ | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| max_range         | Smallint     | -        | -       | Max range for full tank                                                                                                                      |
| wheel_orientation | Varchar(255) | -        | -       | Wheel orientation type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/enums/WheelOrientationType\|WheelOrientationType]] |
| eco_class         | Bytea        | -        |         | Eco class                                                                                                                                    |
| 0_to_100          | Bytea        | -        | -       | acceleration from 0 to 100 (10 ms)                                                                                                           |
| fuel_consumption  | Bytea        | -        | -       | Fuel consumption on 100 km (mixed)                                                                                                           |


```
other_props: [
	max_range: ...,
	wheel_orientation_id: ...,
	eco_class_id: ...,
	0_to_100: ...,
	fuel_consumption: ...
```