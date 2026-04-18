Jsonb with entities list markers

| Field name     | Data                               | Unique | Not Null | Default |
| -------------- | ---------------------------------- | ------ | -------- | ------- |
| countries      | codes and cities                   | -      | -        | -       |
| cities         | ids                                | -      | -        | -       |
| concerns       | ids                                | -      | -        | -       |
| brands         | ids and models                     | -      | -        | -       |
| models         | ids and generations                | -      | -        | -       |
| generations    | ids, variations and complectations |        |          |         |
| variations     | ids                                | -      | -        | -       |
| complectations | ids                                | -      | -        | -       |
| gearboxes      | ids                                | -      | -        | -       |
| engines        | ids                                | -      | -        | -       |
```
entities_list: [
	countries: [
		codes: [...],
		cities: [
			ids: [...]
		]
	],
	concerns: [
		ids: [...]
	],
	brands: [
		ids: [...],
		models: [
			ids: [...],
			generations: [
				ids: [...],
				variations: [...],
				complectations: [...]
			]
		]
	],
	gearboxes: [...],
	engines: [...]
]
```