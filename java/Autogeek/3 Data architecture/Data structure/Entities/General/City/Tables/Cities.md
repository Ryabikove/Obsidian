Table which contains data about [[Autogeek/3 Data architecture/Data structure/Entities/General/City/City|cities]].

| Field name   | Data type    | Unique         | Not Null | Default | Description                                                                                                            |
| ------------ | ------------ | -------------- | -------- | ------- | ---------------------------------------------------------------------------------------------------------------------- |
| id           | Serial       | PK             | +        | -       | ID                                                                                                                     |
| country_code | Varchar(3)   | FK one ot many | +        | -       | Country code from [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Tables/Countries\|countries]] |
| full_name    | Varchar(200) | -              | +        | -       | Full name                                                                                                              |
