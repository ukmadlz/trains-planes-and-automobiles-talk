#  Update

Android:

```java
DocumentRevision rev = datastore.getDocument("droidcon");
MutableDocumentRevision mutable = rev.mutableCopy();
Map<String,Object> body = rev.body.asMap();
body.put("talk","Planes, Trains & Automobiles");
mutable.body = DocumentBodyFactory.create(body);

rev = datastore.updateDocumentFromRevision(mutable);
```


Javascript:

```javascript
db.put(doc, [docId], [docRev], [options], [callback]);

db.get('droidcon', function(err, doc) {
  if (err) { return console.log(err); }
  db.put({
    _id: 'droidcon',
    _rev: doc._rev,
    talk: "Planes, Trains & Automobiles"
  }, function(err, response) {
    if (err) { return console.log(err); }
    // handle response
  });
});
```
