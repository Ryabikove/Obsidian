Entity which represent gearbox.

*Table in DB* - [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Gearbox/Tables/Gearboxes|Gearboxes]]

*Full view:*

| Description                                                                                                                                 | Field name                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Gearbox name                                                                                                                                | full_name                                                                                                                                 |
| Gearbox photos                                                                                                                              | photos                                                                                                                                    |
| Previouis generation parent-gearbox name-link                                                                                               | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Gearbox/Tables/Gearboxes\|gearboxes]] on gearbox_parent_id |
| List of [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Variation\|variations]] name-links which has this gearbox | full_name from [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Variation/Tables/Variations\|variations]] on gearbox_id    |
| Gearbox type                                                                                                                                | gearbox_type                                                                                                                              |
| Gears quantity                                                                                                                              | gear_quantity                                                                                                                             |
| Review                                                                                                                                      | review                                                                                                                                    |

[[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|Full and short views]]

Can't be shows as [[Autogeek/3 Data architecture/Maps/Modules/Secondary/Entity list|entity list]].