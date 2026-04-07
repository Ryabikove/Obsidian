Jsonb which contains offer complectation properties.

| Field name       | Data type    | Unique | Not Null | Default | Description                                                                                                                                |
| ---------------- | ------------ | ------ | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| id               | Serial       | PK     | +        | -       | ID                                                                                                                                         |
| full_name        | Varchar(100) | -      | +        | -       | Name of complectation                                                                                                                      |
| linght_props     | JSONB        | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Light_props\|light props]]           |
| anti-theft_props | JSONB        | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Anti-theft_props\|anti-theft props]] |
| interier_props   | JSONB        | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Interier_props\|interier props]]     |
| safety_props     | JSONB        | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Safety_props\|safety props]]         |
| multimedia_props | JSONB        | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Multimedia_props\|multimedia props]] |
| exterier_props   | JSONB        | -      | +        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Exterier_props\|exterier props]]     |

```
complectation : [
	id: ...,
	full_name: '...',
	light_props: [
		light_auto_correction: [true/false],
		rain_sensor: [true/false],
		light_sensor: [true/false],
		daytime_light: [true/false],
		light_washers: [true/false],
		fog_lights: [true/false],
		light_turning_correction: [true/false],
		light_adaptation_system : [true/false],
		high_light_control_system: [true/false]
	],
	anti-theft_props: [
		central_lock: [false/true],
		immobilizer: [false/true],
		intrusion_sensor: [false/true]
	],
	interier_props: [
		light_auto_correction: [true/false],
		rain_sensor: [true/false],
		light_sensor: [true/false],
		daytime_light: [true/false],
		light_washers: [true/false],
		fog_lights: [true/false],
		light_turning_correction: [true/false],
		light_adaptation_system : [true/false],
		high_light_control_system: [true/false]
	],
	safety_props: [
		abs: [true/false],
		back_doors_lock: [true/false],
		armored_body: [true/false],
		tire_pressure_sensor: [true/false],
		stabilization_system: [true/false],
		ERA-GLONASS: [true/false]
	],
	multimedia_props: [
		aux: [true/false],
		android_auto: [true/false],
		carplay: [true/false],
		usb: [true/false],
		voice_control: [true/false],
		backseat_multimedia: [true/false],
		lcd_screen: [true/false],
		navigation_system : [true/false],
		socket_12v: [true/false],
		socket_220v: [true/false],
		yandex_auto: [true/false]
	],
	exterier_props: [
		aerography: [true/false],
		body_kits: [true/false],
		roof_rails: [true/false]
	]
]
```