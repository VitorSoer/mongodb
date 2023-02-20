1 - Insert 3 patient records with at least 1 history per patient

```console
use hospital

db.patients.insertMany([
    {
        firstName: 'Jhon',
        lastName: 'Doe',
        age: 29,
        history: [
            {
                disease: 'Cold',
                treatment: 'Analgesic'
            },
        ]
    },
    {
        firstName: 'Don',
        lastName: 'Draper',
        age: 45,
        history: [
            {
                disease: 'Cold',
                treatment: 'Analgesic'
            },
        ]
    },
    {
        firstName: 'Eddie',
        lastName: 'Simmons',
        age: 18,
        history: [
            {
                disease: 'Ear infection',
                treatment: 'Antibiotic'
            },
        ]
    },
])
```

2 - Update patient data of 1 patient with new age, name and history entry

```console
db.patients.updateOne(
    { firstName: 'Jhon' },
    { $set: {
        firstName: 'Carl',
        lastName: 'Johnson',
        age: 27,
        history: [
            {
                disease: 'Anemia',
                treatment: 'Vitamin and Pizza'
            },
        ]
    }}
)
```

3 - Find all patients who are older than 30:

```console
db.patients.find({
    age: { $gt: 30 }
}).pretty()
```

4 - Delete all patients who got a cold as a disease:

```console
db.patients.deleteMany({
    'history.disease': 'Cold'
})
```
