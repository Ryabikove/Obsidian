Table which contains data about [[Autogeek/4 UX-projecting/Data structure/Entities/General/Country/Tables/Countries|countries]].

| Field name | Data type    | Unique | Not Null | Default | Description                |
| ---------- | ------------ | ------ | -------- | ------- | -------------------------- |
| iso_code   | Varchar(3)   | PK     | +        | -       | International country code |
| alpha2     | Varchar(2)   | +      | +        | -       | Country code in alpha2     |
| alpha3     | Varchar(3)   | +      | +        | -       | Country code in  alpha3    |
| full_name  | Varchar(200) | -      | +        | -       | Full name                  |
| flag       | Varchar(255) | +      | +        | -       | Link on iamge of flag      |
