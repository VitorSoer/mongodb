1 - Create and switch to database:

```console
use flights
```

2 - Create a collection and insert a document:

```console
db.flightData.insertOne({
    departureAirport: "FRC",
    arrivalAirport: "MNU",
    aircraft: "Airbus A320",
    distance: 20000,
    intercontinental: false,
  })
```

3 - Print all documents:

```console
db.flightData.find().pretty()
```
