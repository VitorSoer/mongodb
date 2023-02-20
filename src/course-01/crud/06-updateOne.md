1 - Update a document:

```console
db.flightData.updateOne(
    { arrivalAirport: "MNU" },
    { $set: { "arrivalAirport" : "BRZ" }}
)
```
