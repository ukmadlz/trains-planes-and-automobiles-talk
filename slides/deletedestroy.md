#  Delete / Destroy


Android:
```java
datastore.deleteDocumentRevision(rev);

// Or

datastore.deleteDocument("droidcon");
```
Javascript:

```Javascript
db.remove(docId, [docRev], [options], [callback]);

db.get('brumjs', function(err, doc) {
  if (err) { return console.log(err); }
  db.remove(doc, function(err, response) {
    if (err) { return console.log(err); }
    // handle response
  });
});
```
