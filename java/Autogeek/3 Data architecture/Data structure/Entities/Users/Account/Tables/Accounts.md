Table which contains information about [[Autogeek/3 Data architecture/Data structure/Entities/Users/Account/Account|accounts]].

| Field name     | Data type                  | Unique         | Not Null | Default | Description                                                                                                        |
| -------------- | -------------------------- | -------------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------------ |
| id             | Serial                     | PK             | +        | -       | ID                                                                                                                 |
| mail           | Varchar(100)               | +              | -        | -       | Email                                                                                                              |
| login          | Varchar(100)               | +              | +        | -       | Login                                                                                                              |
| phone_number   | Varchar(30)                | +              | -        | -       | Phone_number                                                                                                       |
| full_name      | Varchar (250)              | -              | -        | -       | Full name                                                                                                          |
| birth_date     | Date                       | -              | -        | -       | Birth date                                                                                                         |
| account_photo  | Varchar(255)               | +              | -        | -       | Profile photo link                                                                                                 |
| is_corporation | Boolean                    | -              | +        | False   | Is account a corporation                                                                                           |
| create_at      | Timestamp without timezone | -              | +        | Now()   | Account create date                                                                                                |
| last_login     | Timestamp with timezone    | -              | +        | Now()   | Last login                                                                                                         |
| country_code   | Varchar(3)                 | FK many to one | +        | -       | Iso_code from [[Autogeek/3 Data architecture/Data structure/Entities/General/Country/Tables/Countries\|countries]] |
| city_id        | Int                        | FK many to one | -        | -       | Id from [[Autogeek/3 Data architecture/Data structure/Entities/General/City/Tables/Cities\|cities]]                |
| drive_since    | Date                       | -              | -        | -       | Driving since                                                                                                      |
| is_verified    | Boolean                    | -              | +        | False   | Is account verified                                                                                                |
