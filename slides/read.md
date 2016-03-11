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
notes:

    Skip conflicts
    Don't talk too much detail on interceptors
    keep it simple
    talk more about arch in the round about here's how it all looks.
