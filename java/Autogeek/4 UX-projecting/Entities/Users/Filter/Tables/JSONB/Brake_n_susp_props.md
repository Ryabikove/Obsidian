Jsonb which contains filter brake and suspencion properties.

| Field name     | Data type | Not Null | Default | Description                                                                                                                                                     |
| -------------- | --------- | -------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| susp_type_ids  | Bytea     | -        | -       | Suspencion type ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Susp_brake_props/Suspension_types\|suspension_types]] |
| brake_type_ids | Bytea     | -        | -       | Brake type ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Susp_brake_props/Brake_types\|brake_types]]                |

```
engine_props: [
	susp_type_ids: [...],
	brake_type_ids: [...]
]
```