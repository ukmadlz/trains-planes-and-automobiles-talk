#  PUT Create

```
db.put(doc, [docId], [docRev], [options], [callback]);

var doc = {
  _id: "bristech",
  event: "Bristech",
  type: "conference",
  date: "2015-10-15"
}
db.put(doc, function(err, response) {
  if (err) { return console.log(err); }
  // handle response
});
```
