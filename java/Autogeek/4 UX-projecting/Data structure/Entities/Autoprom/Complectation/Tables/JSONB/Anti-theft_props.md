Jsonb which contains anti-theft properies.

| Field name       | Data type | Not Null | Default |
| ---------------- | --------- | -------- | ------- |
| central_lock     | boolean   | +        | False   |
| immobilizer      | boolean   | +        | False   |
| intrusion_sensor | boolean   | +        | False   |

```
anti-theft_props: [
	central_lock: [false/true],
	immobilizer: [false/true],
	intrusion_sensor: [false/true]
]
```