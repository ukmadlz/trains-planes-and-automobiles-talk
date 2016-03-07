#  Changes

Android:

```java
Changes changes = datastore.changes(0, 25);

for (DocumentRevision rev : changes.getResults()){
    // do something with the change
}

// get the next set of changes
changes = datastore.changes(changes.getLastSequence(),25);

//process those changes.
```
