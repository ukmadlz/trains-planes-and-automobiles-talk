#  Query

Javascript MapReduce:


```javascript
// save the design doc
db.put(ddoc, function (err) {
  if (err && err.status !== 409) {
    return console.log(err);
  }
  // ignore if doc already exists
  // find docs where type === 'conference'
  db.query('index', {
    key: 'conference',
    include_docs: true
  }, function (err, result) {
    if (err) { return console.log(err); }
    // handle result
  });
});

// Or use existing DDoc
```
