Entity which represents concern - brands owner.

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concern/Tables/Сoncerns|Сoncerns]]

*Full view:*

| Description                                                                                            | Field name                                                                                                                          |
| ------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                              | full_name                                                                                                                           |
| Logo                                                                                                   | logo                                                                                                                                |
| [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Country\|Country's]] name-link  | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Tables/Countries\|countries]] on country_code |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Brand\|Main brand's]] name-link  | full name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] on main_brand_id       |
| List [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Brand\|brand's]] name-links | full name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] on id                  |
| Capitalization                                                                                         | capitalization                                                                                                                      |
| Grows of capitalization                                                                                | grows                                                                                                                               |
| Description and history                                                                                | description_n_history                                                                                                               |
| List of countries where do the cars produced                                                           | *think about realisation*                                                                                                           |
*Short view:*

| Description                                                                                           | Field name                                                                                                                          |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Short name                                                                                            | short_name                                                                                                                          |
| Logo                                                                                                  | logo                                                                                                                                |
| [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Country\|Country's]] name-link | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Tables/Countries\|countries]] on country_code |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Brand\|Main brand's]] name-link | full name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] on main_brand_id       |
[[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|Full and short views]].

Can be shown as [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]].