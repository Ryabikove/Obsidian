Entity, which describes a review of the entities. 
A review can be created by user. It contains detailed description of cars properties and functions. Unlike reports, review can be created only by user who has a car specialist marker. *how it can be designed*

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/Users/Review/Tables/Reviews|Reviews]].

*Full view:*

| Field name         | Description                                                                                                                                              |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Creation date      | creation_date                                                                                                                                            |
| Variation name     | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Tables/Variations\|variations]] on variation_id                 |
| Complectation name | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] on complectation_id |
| Photos             | photos                                                                                                                                                   |
| Description        | description                                                                                                                                              |
| Rating             | rating                                                                                                                                                   |
| Account            | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Users/Account/Tables/Accounts\|accounts]] on account_id                            |
*Short view:*

| Field name         | Description                                                                                                                                              |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Creation date      | creation_date                                                                                                                                            |
| Variation name     | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Tables/Variations\|variations]] on variation_id                 |
| Complectation name | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] on complectation_id |
| Photos             | photos                                                                                                                                                   |
| Owners             | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Users/Account/Tables/Accounts\|accounts]] on account_id                            |

[[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|Full and short views]].

Can be shown as [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]].