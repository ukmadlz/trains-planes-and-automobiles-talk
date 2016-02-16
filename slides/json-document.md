#  JSON Document

```
var doc = {
  event: "BrumJS",
  type: "conference",
  date: "2015-10-15"
}
```
```java
MutableDocumentRevision revision = new MutableDocumentRevision();
Map<String,String> body = new HashMap<String, String>();
body.put("event", "droidcon";
body.put("type", "conference");
body.put("date", "2016-03-15");
revision.body = DocumentBodyFactory.create(body);
```
