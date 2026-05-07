[[JPA/entity/Entity|Entity]], which describes a review of the entities. 
A review can be created by user. It contains detailed description of cars properties and functions. Unlike reports, review can be created only by user who has a car specialist marker. *how it can be designed*

*Table in DB* - [[Autogeek/4 UX-projecting/Entities/Users/Review/Tables/Reviews|Reviews]].

*Full view:*

| Field name         | Description      |
| ------------------ | ---------------- |
| Creation date      | creation_date    |
| Variation name     | variation_id     |
| Complectation name | complectation_id |
| Photos             | -                |
| Description        | description      |
| Rating             | rating           |
| Account            | account_id       |
*Short view:*

| Field name         | Description      |
| ------------------ | ---------------- |
| Creation date      | creation_date    |
| Variation name     | variation_id     |
| Complectation name | complectation_id |
| Photos             | -                |
| Owners             | account_id       |

[[Autogeek/4 UX-projecting/Entity list|Full and short views]].

Can be shown as [[Autogeek/4 UX-projecting/Entity list|entity list]].