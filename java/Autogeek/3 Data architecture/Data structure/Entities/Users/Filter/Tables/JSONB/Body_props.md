Jsonb which contains filter body properties.

| Field name         | Data type      | Not Null | Default | Description                                                                                                                     |
| ------------------ | -------------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------------- |
| body_length        | Small int list | -        | -       | Body length (mm)                                                                                                                |
| body_width         | Small int list | -        | -       | Body width (mm)                                                                                                                 |
| body_heigth        | Small int list | -        | -       | Body height (mm)                                                                                                                |
| tank_capacity      | Small int list | -        | -       | Tank capacity (l)                                                                                                               |
| min_trunk_capacity | Small int list | -        | -       | Min trunk capacity (l)                                                                                                          |
| max_trunk_capacity | Small int list | -        | -       | Max trunk capacity (l)                                                                                                          |
| seats_quantity     | Bytea list     | -        | -       | Seats quantity                                                                                                                  |
| doors_quantity     | Bytea list     | -        | -       | Door quantity                                                                                                                   |
| empty_weight       | Small int list | -        | -       | Empty weight (kg)                                                                                                               |
| full_weight        | Small int list | -        | -       | Full weight (kg)                                                                                                                |
| wheel_base         | Small int list | -        | -       | Wheel base (mm)                                                                                                                 |
| front_track        | Small int list | -        | -       | Front track (mm)                                                                                                                |
| back_track         | Small int list | -        | -       | Back track (mm)                                                                                                                 |
| body_color         | bytea list     | -        | -       | Body_colors                                                                                                                     |
| color_types        | bytea list     | -        | -       | Color types from [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Body_color_types\|body_color_types]] |

```
body_props: [
	body_length: [...],
	body_width: [...],
	body_heigth: [...],
	tank_capacity: [...],
	min_trunk_capacity: 'val'
	max_trunk_capacity: 'val'
	seats_quantity: 'val'
	doors_quantity: 'val'
	empty_weight: [...]
	full_weight: [...]
	wheel_base: [...]
	front_track: [...]
	back_track: [...]
	body_color: [...],
	color_types: [...],
]
```