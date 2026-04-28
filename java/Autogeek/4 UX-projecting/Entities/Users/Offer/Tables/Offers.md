Table which contains information about [[Autogeek/4 UX-projecting/Entities/Users/Offer/Offer|offers]].

| Field name        | Data type                  | Unique         | Not Null | Default | Description                                                                                                       |
| ----------------- | -------------------------- | -------------- | -------- | ------- | ----------------------------------------------------------------------------------------------------------------- |
| id                | Big serial                 | PK             | +        | -       | Id                                                                                                                |
| seller_account_id | Int                        | FK one to many | +        | -       | Seller's id from table [[Autogeek/4 UX-projecting/Entities/Users/Account/Tables/Accounts\|Accounts]]              |
| city_id           | Int                        | FK one to many | +        | -       | City id from [[Autogeek/4 UX-projecting/Entities/Global/City/Tables/Cities\|cities]]                              |
| variation_id      | Int                        | FK one to many | +        | -       | id from [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Variations\|variations]]                    |
| complectation     | JSONB                      | -              | +        | -       | jsonb with [[Autogeek/4 UX-projecting/Entities/Users/Offer/Tables/JSONB/Complectation\|complectation]] properties |
| offer_type        | Varchar(255)               | -              | +        | -       | Type of offer from [[Autogeek/4 UX-projecting/Entities/Users/Offer/Tables/enums/OfferType\|OfferType]]            |
| price             | Big int                    | -              | +        | -       | Price                                                                                                             |
| photos            | Varchar(255)               | +              | -        | -       | link to photos archive                                                                                            |
| description       | Text                       | -              | -        | -       | Description of offer                                                                                              |
| creation_date     | Timestamp without timezone | -              | +        | NOW()   | Creation date                                                                                                     |
| last_update       | Timestamp without timezone | -              | +        | NOW()   | Last change date                                                                                                  |
| is_actual         | Boolean                    | -              | +        | true    | Is offer actual                                                                                                   |
| was_in_accident   | Boolean                    | -              | +        | false   | Was car in accident                                                                                               |
| mileage           | Small int                  | -              | +        | -       | Mileage of car                                                                                                    |
| vrc_id            | Big int                    | FK one to one  | +        | -       | vehicle registration certificate from [[Autogeek/4 UX-projecting/Entities/Users/Offer/Tables/Vrces\|vrces]]       |
| body_color        | Bytea                      | -              | +        | -       | Color of car                                                                                                      |
| body_color_type   | Bytea                      | FK one to many | +        | -       | Color type from [[Autogeek/4 UX-projecting/Entities/Users/Offer/Tables/enums/BodyColorType\|BodyColorType]]       |
| interior_color    | Bytea                      | -              | +        | -       | Color of car                                                                                                      |
| has_guarantee     | Boolean                    | -              | +        | false   | Car has guarantee                                                                                                 |
| may_change        | Boolean                    | -              | +        | false   | Car may be changed                                                                                                |
*Relations*:

| Mapped entity                                                                         | Column            | Relation type | Fetch type | Cascade | Orhpan removal | Optional |
| ------------------------------------------------------------------------------------- | ----------------- | ------------- | ---------- | ------- | -------------- | -------- |
| [[Autogeek/4 UX-projecting/Entities/Users/Account/Account\|Account]]                  | seller_account_id | Many to one   | EAGER      | REFRESH | -              | false    |
| [[Autogeek/4 UX-projecting/Entities/Global/City/Tables/Cities\|City]]                 | city_id           | Many to one   | LAZY       | REFRESH | -              | false    |
| [[Autogeek/4 UX-projecting/Entities/Autoprom/Variation/Tables/Variations\|Variation]] | variation_id      | One to many   | LAZY       | REFRESH | -              | false    |
| [[Autogeek/4 UX-projecting/Entities/Users/Offer/Tables/Vrces\|Vrc]]                   | vrc_id            | One to one    | LAZY       | REFRESH | -              | false    |
