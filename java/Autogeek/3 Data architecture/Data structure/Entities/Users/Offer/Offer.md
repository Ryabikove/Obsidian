Entity, which describes actual offer from auto-sellers.

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Offers|Offers]].

*Full view:*

| Field name                 | Description                                                                                                                                                  |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Full name                  | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Tables/Variations\|variations]] on variation_id                     |
| Complectation name         | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] on complectation_id     |
| Photos                     | photos                                                                                                                                                       |
| Price                      | price                                                                                                                                                        |
| Type of offer              | offer_type                                                                                                                                                   |
| Year of manufacture        | year_of_manufacture from table [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Vrces\|vrces]] on vrc_id                            |
| Mileage of car             | mileage                                                                                                                                                      |
| Is vrc original            | is_original from table [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Vrces\|vrces]] on vrc_id                                    |
| Owners                     | owners from [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Vrces\|vrces]] on vrc_id                                               |
| Seller's account link-name | id from table [[Autogeek/3 Data architecture/Data structure/Entities/Users/Account/Tables/Accounts\|accounts]] on seller_account_id                          |
| Type of offer              | offer_type_name from [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Offer_types\|offer_types]]                                    |
| Offer creation date        | creation_date                                                                                                                                                |
| Was car in accident        | was_in_accident                                                                                                                                              |
| Car may be changed         | may_change                                                                                                                                                   |
| Car has guarantee          | has_guarantee                                                                                                                                                |
| Description of offer       | description                                                                                                                                                  |
| Characteristics            | * from table [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Tables/Variations\|variations]] on variation_id                       |
| Complectation              | * from table [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/Complectations\|complectations]] on complectation_id       |
| Color of cars body         | body_color                                                                                                                                                   |
| Color of interier          | interier_color                                                                                                                                               |
| Color type                 | Color type name from table [[Autogeek/3 Data architecture/Data structure/Entities/Users/Offer/Tables/Body_color_types\|body_color_types]] on body_color_type |
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