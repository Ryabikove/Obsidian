Jsonb which contains filter offers properties.

| Field name          | Data type | Not Null | Default | Description                                                                                                                             |
| ------------------- | --------- | -------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| full_tank_range     | Small int | -        | -       | Full tank range (km)                                                                                                                    |
| wheel_orientations  | bytea     | -        | -       | Wheel orientation from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/enums/WheelOrientationType\|WheelOrientationType]] |
| eco_classes         | bytea     | -        | -       | Eco class                                                                                                                               |
| fuel_consumpt_range | Small int | -        | -       | Fuel consumption range                                                                                                                  |

```
offer_props: [
	full_tank_range: [...],
	wheel_orientations: [...],
	eco_classes: [...],
	fuel_consumpt_range [...]
]
```