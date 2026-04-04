Сущность, представляющая модель авто.

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Tables/Models|Models]].

*Full view:*

| Description                                                                                                                  | Field name                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                                                    | full_name                                                                                                                         |
| Photos of all generation                                                                                                     | photos                                                                                                                            |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Brand\|Brand]] name-link                               | short_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] on brand_id         |
| List with name-links of [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Generation/Generation\|generations]] | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Generation/Tables/Generations\|generations]] on id |
| Description and history                                                                                                      | description_n_history                                                                                                             |
*Short view:*

| Description                                                                                    | Field name                                                                                                                |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                      | full_name                                                                                                                 |
| Photos of all generation                                                                       | photos                                                                                                                    |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Brand\|Brand]] name-link | short_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] on brand_id |
[[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|Full and short views]].

Can be shown as [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]].