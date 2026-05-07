[[JPA/entity/Entity|Entity]], which describes a article with auto topic. 

An article can be created only by a car specialist and contains information about multiple entities. Unlike reports and reviews, article is created by specialist and moderated by command of product.

*Table in DB* - [[Autogeek/4 UX-projecting/Entities/Users/Article/Tables/Articles|Articles]].

*Full view:*

| Field name         | Description      |
| ------------------ | ---------------- |
| Creation date      | creation_date    |
| Variation name     | variation_id     |
| Complectation name | complectation_id |
| Photos             | -                |
| Content            | content          |
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
#Delayed