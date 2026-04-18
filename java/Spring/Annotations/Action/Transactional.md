Annotation, which gives method property of data base transaction: if smth goes wrong, whole method is rolled back.

Usually used inside [[Spring/Entitites/Service|services]].

```
@Transactional
public void saveWhithEdits(){...}
```