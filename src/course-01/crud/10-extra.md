1 - Create and switch to a database:

```console
use embeddedDB
```

2 - Create a collection and insert the documents:

```console
db.guests.insertMany([
    {
        name: 'Jhon Doe',
        age: 29
    },
    {
        name: 'Martha Doe',
        age: 32
    },
    {
        name: 'Billy Doe',
        age: 11
    }
])
```

03 - Embedded documents:

```console
db.guests.updateMany(
    { age: { $gt: 18 }},
    { $set: {
        status: { description: 'adult' }
    }}
)
```

04 - Arrays:

```console
db.guests.updateOne(
    { name: 'Billy Doe' },
    { $set: { toys: ['Car', 'Soldier'] }}
)
```

05 - Find Embedded documents:

```console
db.guests.find({ "status.description": "adult" })
```

05 - Projection:

```console
db.guests.find({}, { name: 1, _id: 0 }).pretty()
```