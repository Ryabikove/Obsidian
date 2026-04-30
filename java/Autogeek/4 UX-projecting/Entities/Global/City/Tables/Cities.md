Table which contains data about [[Autogeek/4 UX-projecting/Entities/Global/City/City|cities]].

| Field name   | Data type    | Unique         | Not Null | Default | Description                                                                                        |
| ------------ | ------------ | -------------- | -------- | ------- | -------------------------------------------------------------------------------------------------- |
| id           | Serial       | PK             | +        | -       | ID                                                                                                 |
| country_code | Varchar(3)   | FK one ot many | +        | -       | Country code from [[Autogeek/4 UX-projecting/Entities/Global/Country/Tables/Countries\|countries]] |
| full_name    | Varchar(200) | -              | +        | -       | Full name                                                                                          |
*Relations*:

| Mapped entity                                                                  | Column       | Relation type | Fetch type | Cascade | Orhpan removal | Optional |
| ------------------------------------------------------------------------------ | ------------ | ------------- | ---------- | ------- | -------------- | -------- |
| [[Autogeek/4 UX-projecting/Entities/Global/Country/Tables/Countries\|Country]] | country_code | Many to one   | EAGER      | REFRESH | -              | false    |
