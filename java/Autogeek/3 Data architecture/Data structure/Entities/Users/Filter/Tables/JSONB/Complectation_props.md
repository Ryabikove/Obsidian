Jsonb which contains filter complectation properties.

| Field name       | Data type | Not Null | Default | Description                                                                                                                                |
| ---------------- | --------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| linght_props     | JSONB     | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Light_props\|light props]]           |
| anti-theft_props | JSONB     | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Anti-theft_props\|anti-theft props]] |
| interier_props   | JSONB     | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Interier_props\|interier props]]     |
| safety_props     | JSONB     | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Safety_props\|safety props]]         |
| multimedia_props | JSONB     | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Multimedia_props\|multimedia props]] |
| exterier_props   | JSONB     | -        | -       | Jsonb with [[Autogeek/3 Data architecture/Data structure/Entities/Autoprom/Complectation/Tables/JSONB/Exterier_props\|exterier props]]     |

```
complectation_props : [
	light_props: [
		light_auto_correction: true,
		rain_sensor: true,
		light_sensor: true,
		daytime_light: true,
		light_washers: true,
		fog_lights: true,
		light_turning_correction: true,
		light_adaptation_system : true,
		high_light_control_system: true
	],
	anti-theft_props: [
		central_lock: true,
		immobilizer: true,
		intrusion_sensor: true
	],
	interier_props: [
		light_auto_correction: true,
		rain_sensor: true,
		light_sensor: true,
		daytime_light: true,
		light_washers: true,
		fog_lights: true,
		light_turning_correction: true,
		light_adaptation_system : true,
		high_light_control_system: true
	],
	safety_props: [
		abs: true,
		back_doors_lock: true,
		armored_body: true,
		tire_pressure_sensor: true,
		stabilization_system: true,
		ERA-GLONASS: true
	],
	multimedia_props: [
		aux: true,
		android_auto: true,
		carplay: true,
		usb: true,
		voice_control: true,
		backseat_multimedia: true,
		lcd_screen: true,
		navigation_system : true,
		socket_12v: true,
		socket_220v: true,
		yandex_auto: true
	],
	exterier_props: [
		aerography: true,
		body_kits: true,
		roof_rails: true
	]
]
```