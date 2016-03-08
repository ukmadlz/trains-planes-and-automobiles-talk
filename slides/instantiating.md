# Instantiating

Android:
```java
DatastoreManager manager = new DatastoreManager(
  ctx.getDir("cloudantsync", Context.MODE_PRIVATE)
);
Datastore ds = manmager.openDatastore("droidConRo16");
```

javascript:
```javascript
var db = new PouchDB('my_database');
```
