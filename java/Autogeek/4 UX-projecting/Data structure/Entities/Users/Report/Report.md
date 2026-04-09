Entity, which describes a report of the [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Generation/Generation|generation]]. 
A report can be created by a car driver and contains his experience of owning the car.

*Table in DB* - [[Autogeek/4 UX-projecting/Data structure/Entities/Users/Report/Tables/Reports|Reports]].

*Full view:*

| Field name         | Description                                                                                                                                              |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Creation date      | creation_date                                                                                                                                            |
| Variation name     | full_name from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Variation/Tables/Variations\|variations]] on variation_id                 |
| Complectation name | full_name from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] on complectation_id |
| Photos             | photos                                                                                                                                                   |
| Description        | description                                                                                                                                              |
| Rating             | rating                                                                                                                                                   |
| Owners             | full_name from [[Autogeek/4 UX-projecting/Data structure/Entities/Users/Account/Tables/Accounts\|accounts]] on account_id                            |
*Short view:*

| Field name         | Description                                                                                                                                              |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Creation date      | creation_date                                                                                                                                            |
| Variation name     | full_name from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Variation/Tables/Variations\|variations]] on variation_id                 |
| Complectation name | full_name from [[Autogeek/4 UX-projecting/Data structure/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] on complectation_id |
| Photos             | photos                                                                                                                                                   |
| Owners             | full_name from [[Autogeek/4 UX-projecting/Data structure/Entities/Users/Account/Tables/Accounts\|accounts]] on account_id                            |

[[Autogeek/4 UX-projecting/Data structure/Entity list|Full and short views]].

Can be shown as [[Autogeek/4 UX-projecting/Data structure/Entity list|entity list]].