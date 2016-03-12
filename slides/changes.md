#  Changes

```
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
