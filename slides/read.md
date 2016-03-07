#  Read


Android:
```java
datastore.getDocument("droidcon");
```

Javascript:
```javascript
db.get(docId, [options], [callback]);

db.get('droidcon', function(err, doc) {
  if (err) { return console.log(err); }
  // handle doc
});
```
