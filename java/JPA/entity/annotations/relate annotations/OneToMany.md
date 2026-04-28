Annotation which specifies relations between one parent and many children.
Works only if [[JPA/entity/annotations/relate annotations/ManyToOne|ManyToOne]] annotation specify in child entity and may be used only in parent entity.

Has several attributes:
- targetEntity - link to class, which mapped as one. (By default - type of field);
- cascade - list of cascade types. (By default - empty). Cascade works only in one direction;
	There are few cascade types:
	- ALL - cascade all operations;
	- PERSIST - cascade the persist operations. Saves child entities when parent is saved. Ususally is used when parent depends on child for existencel.
	- MERGE - update child entities when parent is updated. Usually is used for maintaining consistency;
	- REMOVE - deletes child entities when parent is deleted. Usually is used when childs cannot exist without parent;
	- REFRESH - reload child entities when parent is refreshed. Usually is used for synchronization with database;
	- DETACH - detach remove child entities from persistence context. Usually is used for manual state management;
- fetch - fetching type. (By default - EAGER)
	There are two fetching types:
	- EAGER - means that entity below must be taken from DB with main entity;
	- LAZY - means that entity below is taken only if it is needed;
- mappedBy - used to specify field name in child entity and make access from parent to child. (By default - empty);
- orphanRemoval - allow to remove child entity by removing entity from relationship with parent;
```
@OneToMany(targetEntity = Country.class,
	cascade = CascadeType.ALL,
	fetch = FetchType.LAZY,
	orphanRemoval = false)
private Country country;
```