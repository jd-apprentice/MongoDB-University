# MongoDB-University

![image](https://user-images.githubusercontent.com/68082746/172720522-c8a34331-1811-4932-9873-0c1f9a736680.png)

# Chapter 3: Creating and Manipulating Documents

### ObjectId

#### How does the value of _id get assigned to a document?

- You can select a non ObjectId type value when inserting a new document, as long as that value is unique to this collection.
- It is automatically generated as an ObjectId type value.

### Insert Errors

- MongoDB can store duplicate documents in the same collection, as long as their _id values are different.
- If a document is inserted without a provided _id value, then the _id field and value will be automatically generated for the inserted document before insertion.

### Insert Order

#### Insert 3 new documents into an empty pets collection

```
db.pets.insert([{ "_id": 1, "pet": "cat" },
                { "_id": 1, "pet": "dog" },
                { "_id": 3, "pet": "fish" },
                { "_id": 4, "pet": "snake" }], { "ordered": false })
```
```
db.pets.insert([{ "pet": "cat" }, { "pet": "dog" },
                { "pet": "fish" }])
```
```
db.pets.insert([{ "_id": 1, "pet": "cat" },
                { "_id": 2, "pet": "dog" },
                { "_id": 3, "pet": "fish" },
                { "_id": 3, "pet": "snake" }])
```

### Updating Documents

#### Examples

```
{ "_id": 1,
  "pet": "cat",
  "attributes": [ { "coat": "fur",
                    "type": "soft" },
                  { "defense": "claws",
                    "location": "paws",
                    "nickname": "murder mittens" } ],
  "name": "Furball" }
```
```
{ "_id": 1,
  "pet": "cat",
  "fur": "soft",
  "claws": "sharp",
  "name": "Furball" }
```
```
{ "_id": 1,
  "pet": "cat",
  "attributes": { "coat": "soft fur",
                  "paws": "cute but deadly" },
  "name": "Furball" }
```

#### Given the following structure 

```
{
 "_id": ObjectId("5ec414e5e722bb1f65a25451"),
 "pet": "wolf",
 "domestic?": false,
 "diet": "carnivorous",
 "climate": ["polar", "equatorial", "continental", "mountain"]
}
```

- How you will add new fields to update the document?

```
db.pets.updateMany({ "pet": "cat" },
                   { "$set": { "type": "dangerous",
                               "look": "adorable" }})
```
```
db.pets.updateMany({ "pet": "cat" },
                   { "$push": { "climate": "continental",
                                "look": "adorable" } })
```

### Deleting Documents

#### Does removing all collections in a database also remove the database?

- Yes once you remove all the collections in a database it removes the db

#### How will you delete a collection named villains?

- db.villains.drop()
