Entity which stores user settings for [[Autogeek/3 Data architecture/Maps/Modules/Main/Filters|filters]] module.

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/Users/Filter/Tables/Filters|Filters]]

*Full view:*

| Field name                      | Description                                                                                                                                              |
| ------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Full name                       | full_name                                                                                                                                                |
| Primary properties              | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] on complectation_id |
| Complectation properties        | price                                                                                                                                                    |
| Offer properties                | offer_type                                                                                                                                               |
| Body properties                 | year_of_manufacture from table [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Vrces\|vrces]] on vrc_id                        |
| Engine properties               | mileage                                                                                                                                                  |
| Gearbox properties              | is_original from table [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Vrces\|vrces]] on vrc_id                                |
| Brake and suspencion properties | owners from [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Vrces\|vrces]] on vrc_id                                           |
| Other properties                | id from table [[Autogeek/3 Data architecture/Data structure/Entities/Users/Account/Tables/Accounts\|accounts]] on seller_account_id                      |

*Short view:*

| Field name                 | Description                                                                                                                         |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Full name                  | var_to_comp_id                                                                                                                      |
| Photos                     | photos                                                                                                                              |
| Price                      | price                                                                                                                               |
| Year of manufacture        | year_of_manufacture from table [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Vrces\|vrces]] on vrc_id   |
| Mileage of car             | mileage                                                                                                                             |
| Seller's account link-name | id from table [[Autogeek/3 Data architecture/Data structure/Entities/Users/Account/Tables/Accounts\|accounts]] on seller_account_id |
| Offer creation date        | creation_date                                                                                                                       |
[[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|Full and short views]].

Can be shown as [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]].