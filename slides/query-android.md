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
