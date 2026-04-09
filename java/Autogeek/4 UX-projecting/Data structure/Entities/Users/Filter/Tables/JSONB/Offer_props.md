Jsonb which contains filter offers properties.

| Field name         | Data type | Not Null | Default | Description                                                                                                              |
| ------------------ | --------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------ |
| owners_quant_range | bytea     | -        | -       | Owners quantity                                                                                                          |
| is_vrc_original    | boolean   | -        | -       | VRC original                                                                                                             |
| offer_type_ids     | bytea     | -        | -       | Offer type ids from [[Autogeek/4 UX-projecting/Data structure/Entities/Users/Offer/Tables/Offer_types\|offer_types]] |
| was_in_accident    | boolean   | -        | -       | Was car in accident                                                                                                      |
| may_be_changed     | boolean   | -        | -       | May car be changed                                                                                                       |
| has_guarantee      | boolean   | -        | -       | Has car a guarantee                                                                                                      |

```
offer_props: [
	owners_quant: [...],
	is_vrc_original: true,
	offer_type_ids: [...],
	was_in_accident: [true\false],
	may_be_changed: true,
	has_guarantee: true
]
```