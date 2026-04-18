Jsonb which contains filter primary properties.

| Field name            | Data type | Not Null | Default | Description                                                                                                                                  |
| --------------------- | --------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| concern_ids           | Int       | -        | -       | Concern ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Concern/Tables/Сoncerns\|concerns]]                         |
| brand_ids             | Int       | -        | -       | Brand ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Brand/Tables/Brands\|brands]]                                 |
| model_ids             | Int       | -        | -       | Model ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Model/Tables/Models\|models]]                                 |
| generation_ids        | Int       | -        | -       | Generation ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Tables/Generations\|generations]]             |
| variation_ids         | Int       | -        | -       | Variation ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Tables/Generations\|generations]]              |
| complectation_ids     | Int       | -        | -       | Complectation ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] |
| price_range           | Big int   | -        | -       | Price range                                                                                                                                  |
| product_years_range   | Small int | -        | -       | Production years range                                                                                                                       |
| dirve_type_ids        | Bytea     | -        | -       | Drive ids type from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Other_props/Drive_types\|drive_types]]  |
| body_type_ids         | Bytea     | -        | -       | Body type ids from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Body_types\|body_types]]                 |
| product_country_codes | Small int | -        | -       | Country of manufacture codes from [[Autogeek/4 UX-projecting/Entities/General/Country/Tables/Countries\|countries]]       |
| 0_to_100              | Bytea     | -        | -       | Acceleration to 100                                                                                                                          |
| consumpt_per_100      | Bytea     | -        | -       | Fuel consumption per 100 km                                                                                                                  |
```
primary_props: [
	concern_ids: [...],
	brand_ids: [...],
	model_ids: [...],
	generation_ids: [...],
	variation_ids: [...],
	complectation_ids: [...],
	price_range: [...],
	product_years_range: [...],
	dirve_type_ids: [...],
	body_type_ids: [...],
	product_country_codes: [...],
	0_to_100_range: [...],
	consumpt_per_100_range: [...]
]
```