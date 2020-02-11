#### write commands for following mongodb opertaions

- create a database named `sports`.
  use sports

- list all databases present in local mongod server.
  show dbs

- create 3 collections named `cricket`, `football`, `TT` in sports databse.
  db.createCollection('cricket')
  db.createCollection('football')
  db.createCollection('TT')

- add multiple players in those collections which should have fields like `name`, `age` and `email` and `cost`.
  db.cricket.insert( {
  ... name: "bim",
  ... age : 24,
  ... email: 'bim240@gmail.com',
  ... cost: 2500000
  ... }) and similar

* list all collections in sports database.
  show collections

* rename `TT` collection to `tennis`.
  db.TT.renameCollection('tennis')

* create a capped collection called `khokho` which should have max 3 documents.
  db.createCollection('khokho', {capped : true, size:4096,max:3})

  Try inserting more than 3 and see what happens?
  db.khokho.insert({player:'bim'})
  db.khokho.insert({player:'bim'})
  db.khokho.insert({player:'bim'})
  db.khokho.insert({player:'bim'})

* check whether a collection is capped or not?
  db.khokho.isCapped()

- drop all documents from `football` collection.
  db.football.remove({})

- delete cricket collection completely.
  db.cricket.drop()

* delete sports database.

ds.dropDatabase()
