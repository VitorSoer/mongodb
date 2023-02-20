1 - Insert documents:

```console
db.flightData.insertMany([{
    departureAirport: "MUC",
    arrivalAirport: "SFO",
    aircraft: "Airbus A380",
    distance: 12000,
    intercontinental: true,
  },
  {
    departureAirport: "LHR",
    arrivalAirport: "TXL",
    aircraft: "Airbus A320",
    distance: 950,
    intercontinental: false,
  }])
```

3 - Print all documents:

```console
db.flightData.find().pretty()
```
