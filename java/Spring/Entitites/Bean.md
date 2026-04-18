Dependency, which creates by spring automatically. Bean is a general entity, based on it creates another entitys.
There are several types of beans:
- [[Spring/Entitites/Service|Service]];
- [[Spring/Entitites/RestController|RestController]];
- [[Spring/Entitites/Reposytory|Reposytory]].

To make Bean from class we use annotations:
- [[Spring/Annotations/Entity/Component|Component]] - makes bean without [[Spring/Entitites/Configuration|configuration]];
- [[Spring/Annotations/Entity/Bean|Bean]] - when need customization of object or create bean from foreign class;

To wire bean with object of main class  is used these annotations:
- [[Spring/Annotations/Action/Autowired|Autowired]];