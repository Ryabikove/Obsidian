Annotation which helps specify foreign key settings.

Has several attributes:
- name - name of foreign key(By default - generated);
- value - constraint mode of value (By default - CONSTRAINT);
	There are three types of value:
	- CONSTRAINT  - apply the constraint.
	- NO_CONSTRAINT - do not apply the constraint. Uses when legacy databases or performance optimization;
	- PROVIDER_DEFAULT - use the provider default behaviour;
- foreignKeyDefinition - string with foreign key definition query (By default - empty);
- options - string with sql fragment which is added to generated DDL(By default - empty);

```
@ForeignKey(
	name = "fk_city_country",
	value = ConstraintMode.CONSTRAINT,
	foreignKeyDefinition = "FOREIGN KEY (country_code) REFERENCES country(code) ON DELETE SET NULL"
)
```