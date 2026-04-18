Table which contains information about [[Autogeek/4 UX-projecting/Entities/Users/Account/Account|accounts]].

| Field name     | Data type                  | Unique         | Not Null | Default | Description                                                                                 |
| -------------- | -------------------------- | -------------- | -------- | ------- | ------------------------------------------------------------------------------------------- |
| id             | Serial                     | PK             | +        | -       | ID                                                                                          |
| mail           | Varchar(100)               | +              | -        | -       | Email                                                                                       |
| login          | Varchar(100)               | +              | +        | -       | Login                                                                                       |
| phone_number   | Varchar(30)                | +              | -        | -       | Phone_number                                                                                |
| full_name      | Varchar (250)              | -              | -        | -       | Full name                                                                                   |
| birth_date     | Date                       | -              | -        | -       | Birth date                                                                                  |
| account_photo  | Varchar(255)               | +              | -        | -       | Profile photo link                                                                          |
| is_corporation | Boolean                    | -              | +        | False   | Is account a corporation                                                                    |
| create_at      | Timestamp without timezone | -              | +        | Now()   | Account create date                                                                         |
| last_online    | Timestamp with timezone    | -              | +        | Now()   | Last login                                                                                  |
| country_code   | Int                        | FK many to one | -        | -       | code from [[Autogeek/4 UX-projecting/Entities/General/Country/Tables/Countries\|countries]] |
| drive_since    | Date                       | -              | -        | -       | Driving since                                                                               |
| is_verified    | Boolean                    | -              | +        | False   | Is account verified                                                                         |
