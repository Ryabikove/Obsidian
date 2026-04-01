Entity, which descrubes actual offer from auto-sellers.

*Table in DB* - [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Offer/Tables/Offers|Offers]]

*Full presentation:*

| Field name                 | Description                                                                                                                                                               |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Full name                  | var_to_comp_id                                                                                                                                                            |
| Photos                     | photos                                                                                                                                                                    |
| Price                      | price                                                                                                                                                                     |
| Type of offer              | offer_type                                                                                                                                                                |
| Year of manufacture        | year_of_manufacture from table [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Offer/Tables/Vrces\|vrces]] on vrc_id                            |
| Mileage of car             | mileage                                                                                                                                                                   |
| Is vrc original            | is_original from table [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Offer/Tables/Vrces\|vrces]] on vrc_id                                    |
| Owners                     | owners from [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Offer/Tables/Vrces\|vrces]] on vrc_id                                               |
| Seller's account link-name | id from table [[Autogeek/3 Data architecture/Структура данных/Сущности/Пользовательские/Account/Tables/Accounts\|accounts]] on seller_account_id                  |
| Type of offer              | offer_type_name from [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Offer/Tables/Offer_types\|offer_types]]                                    |
| Offer creation date        | creation_date                                                                                                                                                             |
| Was car in accident        | was_in_accident                                                                                                                                                           |
| Car may be changed         | may_change                                                                                                                                                                |
| Car has guarantee          | has_guarantee                                                                                                                                                             |
| Description of offer       | description                                                                                                                                                               |
| Characteristics            | * from table [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Вариация/Таблицы/Characteristics\|characteristics]] on var_to_comp_id              |
| Complectation              | * from table [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Комплектация/Таблицы/Complectations\|complectations]] on var_to_comp_id            |
| Color of cars body         | body_color                                                                                                                                                                |
| Color of interier          | interier_color                                                                                                                                                            |
| Color type                 | Color type name from table [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Offer/Tables/Body_color_types\|cody_color_types]] on body_color_type |

*Short presentation:*

| Field name                 | Description                                                                                                                                              |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Full name                  | var_to_comp_id                                                                                                                                           |
| Photos                     | photos                                                                                                                                                   |
| Price                      | price                                                                                                                                                    |
| Year of manufacture        | year_of_manufacture from table [[Autogeek/3 Data architecture/Структура данных/Сущности/Автопром/Offer/Tables/Vrces\|vrces]] on vrc_id           |
| Mileage of car             | mileage                                                                                                                                                  |
| Seller's account link-name | id from table [[Autogeek/3 Data architecture/Структура данных/Сущности/Пользовательские/Account/Tables/Accounts\|accounts]] on seller_account_id |
| Offer creation date        | creation_date                                                                                                                                            |
[[Autogeek/3 Data architecture/Карты/Модули/Дополнительные/Список сущностей|Full and short presentation]]

Can be shown like [[Autogeek/3 Data architecture/Карты/Модули/Дополнительные/Список сущностей|entity list]]