[[Autogeek/4 UX-projecting/Entity|Entity]] which describes model of car.

*Table in DB* - [[Autogeek/4 UX-projecting/Entities/Autoprom/Model/Tables/Models|Models]].

*Full view:*

| Description                                                                                                                  | Field name                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                                                    | full_name                                                                                                                         |
| Photos of all generation                                                                                                     | photos                                                                                                                            |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Brand/Brand\|Brand]] name-link                               | short_name from [[Autogeek/4 UX-projecting/Entities/Autoprom/Brand/Tables/Brands\|brands]] on brand_id         |
| List with name-links of [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Generation\|generations]] | full_name from [[Autogeek/4 UX-projecting/Entities/Autoprom/Generation/Tables/Generations\|generations]] on id |
| Description and history                                                                                                      | description_n_history                                                                                                             |
*Short view:*

| Description                                                                                    | Field name                                                                                                                |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                      | full_name                                                                                                                 |
| Photos of all generation                                                                       | photos                                                                                                                    |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Brand/Brand\|Brand]] name-link | short_name from [[Autogeek/4 UX-projecting/Entities/Autoprom/Brand/Tables/Brands\|brands]] on brand_id |
[[Autogeek/4 UX-projecting/Entity list|Full and short views]].

Can be shown as [[Autogeek/4 UX-projecting/Entity list|entity list]].