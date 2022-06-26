# MongoDB-University

![image](https://user-images.githubusercontent.com/68082746/172720522-c8a34331-1811-4932-9873-0c1f9a736680.png)

# Chapter 4 Advanced CRUD Operations

### Comparison Operators

```
Problem:

To complete this exercise connect to your Atlas cluster using the in-browser IDE space at the end of this chapter.

How many documents in the sample_training.zips collection have fewer than 1000 people listed in the pop field?

Copy/paste the exact numeric value (without double quotes) of the result that you get into the response field.
```

```sql
db.zips.find({ "pop": { "$lt": 1000 }}).count()
```
- The query above finds in the `zips` db where the attribute "pop" is lower then 1000

###############################################################################################################
```
Problem:

To complete this exercise connect to your Atlas cluster using the in-browser IDE space at the end of this chapter.

What is the difference between the number of people born in 1998 and the number of people born after 1998 in the sample_training.trips collection?

Enter the exact numeric value of the result that you get into the response field.
```

- To solve this exercise we need to create 2 queries one for the people who exactly born in 1998 and other for the people who is born after 1998

```sql
db.trips.find({"birth year": {"$gt": 1998}}).count()
```
- The query above returns 18
```sql
db.trips.find({"birth year": {"$eq": 1998}}).count()
```
- The query abone retunrs 12

#### The solution here is 6, which is the difference between 18 and 12

##########################################################################
```
Problem:

To complete this exercise connect to your Atlas cluster using the in-browser IDE space at the end of this chapter.

Using the sample_training.routes collection find out which of the following statements will return all routes that have at least one stop in them?
```

```sql
db.routes.find({ "stops": { "$ne": 0 }}).pretty()
```
- The given query looks for strict equality where the stops field has to be greater than zero, thus excluding all zero stops.

```sql 
db.routes.find({ "stops": { "$gt": 0 }}).pretty()
```
- This query will also work, given that there are no non-negative or non- numeric values in this collection. It returns all documents where the stops field is not equal to 0.
