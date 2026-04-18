Jsonb which contains suspension and brake properties.

| Field name            | Data type | Not Null | Default | Description                                                                                                                                                       |
| --------------------- | --------- | -------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| front_suspension_type | bytea     | -        | -       | Front suspension type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Susp_brake_props/Suspension_types\|suspension_types]] |
| back_suspension_type  | bytea     | -        | -       | Back suspension type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Susp_brake_props/Suspension_types\|suspension_types]]  |
| back_brake_type       | bytea     | -        | -       | Back brake type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Susp_brake_props/Brake_types\|brake_types]]                 |
| front_brake_type      | bytea     | -        | -       | Front brake type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Susp_brake_props/Brake_types\|brake_types]]                |

```
susp_brake_props: [
	front_suspension_type: ...,
	back_suspension_type: ...,
	back_brake_type: ...,
	front_brake_type: ...
]
```