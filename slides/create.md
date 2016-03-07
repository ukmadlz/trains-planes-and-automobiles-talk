#  Create

Android:

```java
DocumentRevision rev = datastore.createDocumentFromRevision(revision);
```

Javascript:

```javascript
db.post(doc, [options], [callback]);

db.post(doc, function (err, response) {
  if (err) { return console.log(err); }
  // handle response
});
```
