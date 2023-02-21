1 - Start mongo server:
```console
mongo
```

2 - Show Databases:
```console
show dbs
```

3 - Create and switch to a database:
```console
use fictionalDB
```

4 - Show current database:
```console
db
```

5 - Create a collection and insert a document:
```console
db.fictionalCollection.insertOne({
    description: 'Fictional data'
}) 
```

6 - Print all documents:
```console
db.fictionalCollection.find()
```
