Entity which represent generation of car model.

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Generation/Tables/Generations|Generations]].

*Full view:*

| Description                                                                                                                                   | Field name                                                                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                                                                     | full_name                                                                                                                                       |
| Generation photos                                                                                                                             | photos                                                                                                                                          |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Brand\|Brands]] name-link                                               | short_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] on brand_id                       |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Model\|Models]] name-link                                               | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Tables/Models\|models]] on model_id                        |
| Years of producing                                                                                                                            | year_start - year_stop                                                                                                                          |
| Description and review                                                                                                                        | description_n_review                                                                                                                            |
| Amount of produced autos                                                                                                                      | produced_auto                                                                                                                                   |
| Amount of sold autos                                                                                                                          | sold_auto                                                                                                                                       |
| Prices range                                                                                                                                  | prices_range                                                                                                                                    |
| Table with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Variation\|variations]] and properties                   | all properties from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Tables/Variations\|variations]] on id             |
| Table with name-links of [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Complectation\|complectations]]        | all properties from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] on id |
| List of [[Autogeek/3 Data architecture/Data structure/Entities/Users/Report/Report\|reports]] in short view                                   | * from [[Autogeek/3 Data architecture/Data structure/Entities/Users/Report/Tables/Reports\|reports]] on generation_id                           |
| List with name-links of [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Country\|countries]]  where autos are produced | *think about realization later*                                                                                                                 |

*Short view:*

| Description                                                                                     | Field name                                                                                                                |
| ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                       | full_name                                                                                                                 |
| Generation photos                                                                               | photos                                                                                                                    |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Brand\|Brands]] name-link | short_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] on brand_id |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Model\|Models]] name-link | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Tables/Models\|models]] on model_id  |
[[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|Full and short views]].

Can be shown as [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]].