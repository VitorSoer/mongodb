1 - Update multiple documents:

```console
db.flightData.updateMany(
    { intercontinental: false },
    { $set: { intercontinental: true }}
)
```
