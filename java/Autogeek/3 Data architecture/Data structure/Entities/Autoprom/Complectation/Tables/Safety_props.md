Table wich contains safety properties.

| Field name           | Data type | Unique | Not Null | Default | Description                     |
| -------------------- | --------- | ------ | -------- | ------- | ------------------------------- |
| id                   | Serial    | PK     | +        | -       | Идентификатор                   |
| abs                  | boolean   | -      | +        | False   | Антиблокировочная система       |
| back_doors_lock      | boolean   | -      | +        | False   | Блокировка замков задних дверей |
| armored_body         | boolean   | -      | +        | False   | Бронированный кузов             |
| tire_pressure_sensor | boolean   | -      | +        | False   | Датчик давления в шинах         |
| stabilization_system | boolean   | -      | +        | False   | Система стабилизации            |
| ERA-GLONASS          | boolean   | -      | +        | False   | ЭРА-ГЛОНАСС                     |

