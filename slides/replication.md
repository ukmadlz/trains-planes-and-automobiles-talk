#  Replication

Android:

```java
URL remoteDB = new URL("http://example.com/db");

// pull
Replicator pull = ReplicatorBuilder.pull().from(remoteDB).to(datastore).build();
pull.start();

// push
Replicator push = ReplicatorBuilder.push().from(datastore).to(remoteDB).build();
push.start();

```

Javascript:

```
PouchDB.replicate(source, target, [options]);

db.replicate.to(remoteDB, [options]);
// or
db.replicate.from(remoteDB, [options]);
```
