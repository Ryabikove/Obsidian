Jsonb which contains filter gearbox properties.

| Field name          | Data type | Not Null | Default | Description                                                                                                                         |
| ------------------- | --------- | -------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| gearbox_type_ids    | Bytea     | -        | -       | Gearbox type ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Gearbox/Tables/Gearbox_types\|gearbox_types]] |
| gear_quantity_range | Bytea     | -        | -       | Quantity of gears                                                                                                                   |

```
engine_props: [
	gearbox_type_ids: [...],
	gear_quantity_range: [...]
]
```