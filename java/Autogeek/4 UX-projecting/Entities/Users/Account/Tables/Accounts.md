Table which contains information about [[Autogeek/4 UX-projecting/Entities/Users/Account/Account|accounts]].

| Field name     | Data type               | Unique         | Not Null | Default | Description                                                                                |
| -------------- | ----------------------- | -------------- | -------- | ------- | ------------------------------------------------------------------------------------------ |
| id             | Bigint                  | PK             | +        | -       | ID                                                                                         |
| mail           | Varchar(100)            | +              | -        | -       | Email                                                                                      |
| login          | Varchar(100)            | +              | +        | -       | Login                                                                                      |
| phone_number   | Varchar(30)             | +              | -        | -       | Phone_number                                                                               |
| full_name      | Varchar (250)           | -              | -        | -       | Full name                                                                                  |
| birthday       | Date                    | -              | -        | -       | Birth date                                                                                 |
| account_photos | Varchar(255)            | +              | -        | -       | Profile photo link                                                                         |
| is_corporation | Boolean                 | -              | +        | False   | Is account a corporation                                                                   |
| create_at      | DATE                    | -              | +        | Now()   | Account create date                                                                        |
| last_online    | Timestamp with timezone | -              | +        | Now()   | Last login                                                                                 |
| country_code   | VARCHAR(3)              | FK many to one | -        | -       | code from [[Autogeek/4 UX-projecting/Entities/Global/Country/Tables/Countries\|countries]] |
| drive_since    | Date                    | -              | -        | -       | Driving since                                                                              |
| is_verified    | Boolean                 | -              | +        | False   | Is account verified                                                                        |
*Relations*:

| Mapped entity                                                                  | Column       | Relation type | Fetch type | Cascade | Orhpan removal | Optional |
| ------------------------------------------------------------------------------ | ------------ | ------------- | ---------- | ------- | -------------- | -------- |
| [[Autogeek/4 UX-projecting/Entities/Global/Country/Tables/Countries\|Country]] | country_code | Many to one   | EAGER      | REFRESH | -              | false    |
| [[Autogeek/4 UX-projecting/Entities/Users/Offer/Tables/Offers\|Offer]]         | -            | One to many   | LAZY       | ALL     | true           | -        |
| [[Autogeek/4 UX-projecting/Entities/Users/Report/Tables/Reports\|Report]]      | -            | One to many   | LAZY       | ALL     | true           | -        |
| [[Autogeek/4 UX-projecting/Entities/Users/Review/Tables/Reviews\|Review]]      | -            | One to many   | LAZY       | ALL     | true           | -        |
