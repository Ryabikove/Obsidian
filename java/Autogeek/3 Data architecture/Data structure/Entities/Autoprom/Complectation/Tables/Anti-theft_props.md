Table wich contains exterier properies.

| Field name       | Data type | Unique | Not Null | Default | Description                      |
| ---------------- | --------- | ------ | -------- | ------- | -------------------------------- |
| id               | Serial    | PK     | +        | -       | Id                               |
| central_lock     | boolean   | -      | +        | False   | Central lock                     |
| immobilizer      | boolean   | -      | +        | False   | Immobilizer                      |
| intrusion_sensor | boolean   | -      | +        | False   | Intrusion sensor (volume sensor) |
