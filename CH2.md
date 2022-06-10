# MongoDB-University

![image](https://user-images.githubusercontent.com/68082746/172720522-c8a34331-1811-4932-9873-0c1f9a736680.png)

# Chapter 2: Importing, Exporting, and Querying Data

### What is JSON?

#### How do it looks a valid JSON?

- A valid JSON would be something like this -> ```{"name" : "Devi", "age": 19, "major": "Computer Science"}```
- They are key: value pairs

#### Whats the difference between BJSON & JSON?

```
MongoDB stores data in BSON,and you can then view it in JSON
BSON is faster to parse and lighter to store than JSON
JSON supports fewer data types than BSON
```

#### Import and Export

- ```mongoimport``` is used for importing a collection that was previously exported with ```mongoexport```
- ```mongoexport``` is used for exporting a collection
- ```mongorestore``` is used for importing a dump that was previously generated with ```mongodump```
- ```mongodump``` is used for generating a dump of a database or any collection

### Documentacion for each of the elements above here

- [import](https://www.mongodb.com/docs/database-tools/mongoimport/)
- [export](https://www.mongodb.com/docs/database-tools/mongoexport/)
- [restore](https://www.mongodb.com/docs/database-tools/mongorestore/)
- [dump](https://www.mongodb.com/docs/database-tools/mongodump/)

#### Data Explorer

- Problem
```
In the sample_training.trips collection a person with birth year 1961 took a trip that started at "Howard St & Centre St". What was the end station name for that trip?
Copy and paste your answer from the Atlas UI to the response text box. The station name should be in a single set double quotes, exactly as it is in the Data Explorer.
```
- The query for this particular problem is ```{"start station name" : "Howard St & Centre St", "birth year" : 1961}```
- The name for what the problem wants is -> ```South End Ave & Liberty St```

### Find Command

#### What does it do in the mongo shell?

- Iterates through the cursor results

### The mongo shell

#### Which of the following statements are true about the mongo shell?

- It allows you to interact with your MongoDB instance without using a Graphical User Interface
- It is a fully functioning JavaScript interpreter
