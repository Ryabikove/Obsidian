Entity which represent country in general

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Tables/Countries|Countries]].
*Full view:*

| Description                                                                                                         | Field name                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Full name                                                                                                           | full_name                                                                                                                       |
| Image of flag                                                                                                       | flag                                                                                                                            |
| List with name-links of [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concern/Concern\|concerns]] | short_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Concern/Tables/Сoncerns\|concerns]] on iso_code |
| List with name-links of [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Brand\|brands]]       | short_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Brand/Tables/Brands\|brands]] on iso_code       |

*Short view:*

| Description   | Field name |
| ------------- | ---------- |
| Full name     | full_name  |
| Image of flag | flag       |
[[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|Full and short view]].

Can be shown as [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]].