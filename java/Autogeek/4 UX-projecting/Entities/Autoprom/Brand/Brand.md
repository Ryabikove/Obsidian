[[Autogeek/4 UX-projecting/Entity|Entity]] which represent an auto brand.

*Table in DB* - [[Autogeek/4 UX-projecting/Entities/Autoprom/Brand/Tables/Brands|brands]].

*Full view:*

| Description                                                                                               | Field name                                                                                                                          |
| --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                                 | full_name                                                                                                                           |
| Logo                                                                                                      | logo                                                                                                                                |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Concern/Concern\|Concern]] name-link      | full_name from [[Autogeek/4 UX-projecting/Entities/Autoprom/Concern/Tables/Сoncerns\|concerns]] on concern_id    |
| [[Autogeek/4 UX-projecting/Entities/General/Country/Country\|Country]] name-link       | full_name from [[Autogeek/4 UX-projecting/Entities/General/Country/Tables/Countries\|countries]] on country_code |
| List of [[Autogeek/4 UX-projecting/Entities/Autoprom/Model/Model\|model's]] name-links | full_name from [[Autogeek/4 UX-projecting/Entities/Autoprom/Model/Tables/Models\|models]] on model_id            |
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
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Concern/Concern\|Concern]] name-link | full_name from [[Autogeek/4 UX-projecting/Entities/Autoprom/Concern/Tables/Сoncerns\|concerns]] on concern_id    |
| Logo                                                                                                 | logo                                                                                                                                |
| [[Autogeek/4 UX-projecting/Entities/General/Country/Country\|Country]] name-link  | full_name from [[Autogeek/4 UX-projecting/Entities/General/Country/Tables/Countries\|countries]] on country_code |
[[Autogeek/4 UX-projecting/Entity list|Full and short view]]

Can be shown as [[Autogeek/4 UX-projecting/Entity list|entity list]]