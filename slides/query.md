#  Query

Android:

```java
IndexManager indexManager = new IndexManager(datastore);

Object[] fields = {"conference"};
indexManager.ensureIndexedArrays.toList(fields), "conference");

Map<String,Object> selector = new HashMap<String,Object>();
selector.put("conference","droidcon");
QueryResult result = indexManager.find(selector);

for(DocumentRevision rev:result){
    // do something with the found document.
}

```

## MapReduce

```
db.query(fun, [options], [callback]);

// create a design doc
var ddoc = {
  _id: '_design/index',
  views: {
    index: {
      map: function mapFun(doc) {
        if (doc.type) {
          emit(doc.type);
        }
      }.toString()
    }
  }
}

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
