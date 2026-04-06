Entity which represent an auto brand.

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands|brands]].

*Full view:*

| Description                                                                                               | Field name                                                                                                                          |
| --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                                 | full_name                                                                                                                           |
| Logo                                                                                                      | logo                                                                                                                                |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concern/Concern\|Concern]] name-link      | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concern/Tables/Сoncerns\|concerns]] on concern_id    |
| [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Country\|Country]] name-link       | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Tables/Countries\|countries]] on country_code |
| List of [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Model\|model's]] name-links | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Model/Tables/Models\|models]] on model_id            |
| Capitalization                                                                                            | capitalization                                                                                                                      |
| Growth rates                                                                                              | growth                                                                                                                              |
| Brand's description and history                                                                           | description_n_history                                                                                                               |
| How many cars were produced                                                                               | produced_auto                                                                                                                       |
| How many cars were sold                                                                                   | sold_auto                                                                                                                           |
| List of countries where do the cars produced                                                              | *think about realisation later*                                                                                                     |
*Short view:*

| Description                                                                                          | Field name                                                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Short name                                                                                           | short_name                                                                                                                          |
| [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concern/Concern\|Concern]] name-link | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concern/Tables/Сoncerns\|concerns]] on concern_id    |
| Logo                                                                                                 | logo                                                                                                                                |
| [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Country\|Country]] name-link  | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Tables/Countries\|countries]] on country_code |
[[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|Full and short view]]

Can be shown as [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]]