#  Query

Javascript Design Doc:

```javascript
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
```
