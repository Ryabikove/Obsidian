Contains vehicle registration certificates.

| Column name         | Data type  | Unique | Not Null | Default | Description         |
| ------------------- | ---------- | ------ | -------- | ------- | ------------------- |
| id                  | Big serial | PK     | +        | -       | ID                  |
| is_original         | Boolean    | -      | +        | false   | Is vrs original     |
| year_of_manufacture | Date       | -      | +        | -       | Year of manufacture |
| owners              | JSONB      | -      | +        | -       | Owners              |
