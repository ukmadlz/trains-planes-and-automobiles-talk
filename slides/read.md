#  Read

```
db.get(docId, [options], [callback]);

db.get('droidcon', function(err, doc) {
  if (err) { return console.log(err); }
  // handle doc
});
```
```java
datastore.getDocument("droidcon");
```
