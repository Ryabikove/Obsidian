Таблица с обзорно-световыми характеристиками комплектации.

| Field name                | Data type | Unique | Not Null | Default | Description                                        |
| ------------------------- | --------- | ------ | -------- | ------- | -------------------------------------------------- |
| id                        | Serial    | PK     | +        | -       | Идентификатор                                      |
| light_auto_correction     | boolean   | -      | +        | False   | Автоматическая корректировка фар                   |
| rain_sensor               | boolean   | -      | +        | False   | Датчик дождя                                       |
| light_sensor              | boolean   | -      | +        | False   | Датчик света                                       |
| daytime_light             | boolean   | -      | +        | False   | Дневные ходовые огни                               |
| light_washers             | boolean   | -      | +        | False   | Омыватель фар                                      |
| fog_lights                | boolean   | -      | +        | False   | Противотуманные фары                               |
| light_turning_correction  | boolean   | -      | +        | False   | Система адаптивного головного освещения в повороте |
| light_adaptation_system   | boolean   | -      | +        | False   | Система адаптивного освещения                      |
| high_light_control_system | boolean   | -      | +        | False   |                                                    |