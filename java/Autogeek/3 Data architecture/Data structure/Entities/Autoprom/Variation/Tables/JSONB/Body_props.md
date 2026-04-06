Jsonb which contains data about car body.

| Field name         | Data type | Unique | Not Null | Default | Description            |
| ------------------ | --------- | ------ | -------- | ------- | ---------------------- |
| body_length        | Smallint  | -      | +        | -       | Body length (mm)       |
| body_width         | Smallint  | -      | +        | -       | Body width (mm)        |
| body_heigth        | Smallint  | -      | +        | -       | Body height (mm)       |
| wheel_base         | Smallint  | -      | +        | -       | Wheel base (mm)        |
| front_track        | Smallint  | -      | +        | -       | Front track (mm)       |
| back_track         | Smallint  | -      | +        | -       | Back track (mm)        |
| doors_number       | Bytea     | -      | +        | -       | Doors number           |
| seats_number       | Bytea     | -      | +        | -       | Seats number           |
| empty_weight       | Smallint  | -      | +        | -       | Empty weight (kg)      |
| full_weight        | Smallint  | -      | +        | -       | Full weight (kg)       |
| min_trunk_capacity | Smallint  | -      | +        | -       | Min trunk capacity (l) |
| max_trunk_capacity | Smallint  | -      | +        | -       | Max trunk capacity (l) |
| tank_capacity      | Smallint  | -      | +        | -       | Tank capacity (l)      |
```
interier_props: [
	body_length: ...,
	body_width: ...,
	body_heigth: ...,
	wheel_base: ...,
	front_track: ...,
	back_track: ...,
	doors_number: ...,
	seats_number : ...,
	empty_weight: ...,
	full_weight: ...,
	min_trunk_capacity: ...,
	max_trunk_capacity: ...,
	tank_capacity: ...
]
```