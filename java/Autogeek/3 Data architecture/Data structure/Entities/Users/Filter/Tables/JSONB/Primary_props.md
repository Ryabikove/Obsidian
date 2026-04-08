Jsonb which contains filter primary properties.

| Field name            | Data type      | Not Null | Default | Description                                                                                                                                  |
| --------------------- | -------------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| concern_ids           | Int list       | -        | -       | Concern ids from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concern/Tables/Сoncerns\|concerns]]                         |
| brand_ids             | Int list       | -        | -       | Brand ids from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]]                                 |
| model_ids             | Int list       | -        | -       | Model ids from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Tables/Models\|models]]                                 |
| generation_ids        | Int list       | -        | -       | Generation ids from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Generation/Tables/Generations\|generations]]             |
| variation_ids         | Int list       | -        | -       | Variation ids from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Generation/Tables/Generations\|generations]]              |
| complectation_ids     | Int list       | -        | -       | Complectation ids from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] |
| price_range           | Big int list   | -        | -       | Price range                                                                                                                                  |
| product_years         | Small int list | -        | -       | Production years range                                                                                                                       |
| dirve_type_ids        | Bytea list     | -        | -       | Drive ids type from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Tables/Other_props/Drive_types\|drive_types]]  |
| body_type_ids         | Bytea list     | -        | -       | Body type ids from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Tables/Body_types\|body_types]]                 |
| product_country_codes | Small int list | -        | -       | Country of manufacture codes from [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Tables/Countries\|countries]]       |
| 0_to_100              | Bytea          | -        | -       | Acceleration to 100                                                                                                                          |
| consumpt_per_100      | Bytea          | -        | -       | Fuel consumption per 100 km                                                                                                                  |
```
primary_props: [
	concern_ids: [...],
	brand_ids: [...],
	model_ids: [...],
	generation_ids: [...],
	variation_ids: [...],
	complectation_ids: [...],
	price_range: [...],
	product_years: [...],
	dirve_type_ids: [...],
	body_type_ids: [...],
	product_country_codes: [...],
	0_to_100: 'val',
	consumpt_per_100: 'val'
]
```