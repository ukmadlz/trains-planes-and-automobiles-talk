#  JSON Document

Android:
```java
MutableDocumentRevision revision = new MutableDocumentRevision();
Map<String,String> body = new HashMap<String, String>();
body.put("event", "droidcon";
body.put("type", "conference");
body.put("date", "2016-03-12");
revision.body = DocumentBodyFactory.create(body);
```

Javascript:
```
var doc = {
  event: "droidcon",
  type: "conference",
  date: "2016-03-12"
}
```
