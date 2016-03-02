#  Changes

Android:

```java
Changes changes = ds.changes(0, 25);

for (DocumentRevision rev : changes.getResults()){
    // do something with the change
}

// get the next set of changes
changes = ds.changes(changes.getLastSequence(),25);

//process those changes.
```

```javascript
db.changes(options);

var changes = db.changes({
  since: 'now',
  live: true,
  include_docs: true
}).on('change', function(change) {
  // handle change
}).on('complete', function(info) {
  // changes() was canceled
}).on('error', function (err) {
  console.log(err);
});

changes.cancel();
```
