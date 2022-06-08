# MongoDB-University

![image](https://user-images.githubusercontent.com/68082746/172720522-c8a34331-1811-4932-9873-0c1f9a736680.png)

# Chapter 1 - What is MongoDB?

- MongoDB is a document database designed for ease of development and scaling.

### Why is MongoDB a NoSQL database?

- Because it uses a structured way to store and access data
- Because it does not utilize tables, rows and columns to organize data

### What is the MongoDB Database?

- The MongoDB database is an organized way to store and access data.
- MongoDB is a NoSQL database that uses documents to store data in an organized way.

### What is a Document?

#### In MongoDB how does a document relate to a collection?

- Collections consist of one or many documents.

##### In MongoDB how does a document relate to a collection?

- A field is a unique identifier for a specific datapoint.
- Each field has a value associated with it.

### What is Atlas?

#### How is MongoDB Atlas related to MongoDB the Database?

- Atlas has many tools and services within it that are built specifically for the MongoDB Database.
- They both are MongoDB products.

#### Create a Cluster and configure it ->

![image](https://user-images.githubusercontent.com/68082746/172724204-1deac8ba-f967-474c-a4fd-35ccc1c71569.png)

The following 10 easy steps will guide you in creating:

- an Atlas Organization named MDBU
- a Project within MDBU called M001
- a Free Tier Atlas cluster named Sandbox

- 1. Select Create an Organization

![image](https://user-images.githubusercontent.com/68082746/172724370-b971751a-38aa-4813-a541-c6a8b62bb87d.png)

- 2. Name your Organization MDBU. Make sure that your cloud service is Atlas, then hit Next.

![image](https://user-images.githubusercontent.com/68082746/172724419-a995414a-ced0-40dd-8cd5-7fd6925e5b1d.png)

- 3. Hit Create Organization

![image](https://user-images.githubusercontent.com/68082746/172724550-336744be-b0d3-4d45-82a4-8324670bed3c.png)

- 4. Hit New Project

![image](https://user-images.githubusercontent.com/68082746/172724577-85ae1727-974c-44a9-bb92-78119ca805d4.png)

- 5. Name your Project M001 and hit Next

![image](https://user-images.githubusercontent.com/68082746/172724608-fd0c3251-c6fb-4e05-9d9d-af7c7b33949f.png)

- 6. Select Create Project

![image](https://user-images.githubusercontent.com/68082746/172724638-1a2e1875-b75f-4ef2-80a7-89a2e26ab529.png)

- 7. Select Build a Database

![image](https://user-images.githubusercontent.com/68082746/172724677-39cc89ff-6f58-4bd5-bb51-1df6b276b7c3.png)

- 8. Select the right-most option that is FREE and hit Create

![image](https://user-images.githubusercontent.com/68082746/172724711-d35926af-f09e-4944-bf95-f0d4df6569a4.png)

- 9. Select the region that is geographically closest to your location. On the bottom of the page change the cluster name to Sandbox. Create the cluster. This step might take a minute or two to complete.

![image](https://user-images.githubusercontent.com/68082746/172724743-1e7f2388-8a64-4317-af01-cb997cad80d6.png)

```Now that you have an Atlas cluster you need to grant access to your IP Address and create a Database User.

You should see Security Quickstart now.

With Username and Password selected, create a user for your database with the following username and password

- username: <YourUser>
- password: <YourPassword>
- Click on Create User
```
![image](https://user-images.githubusercontent.com/68082746/172725020-f3152ace-f5d1-4414-a687-d50e13d45dd6.png)

- Select the option on the left My Local Environment and add an entry under Add entries to your IP Access List. Add your local IP address 0.0.0.0/0 and click Add Entry

![image](https://user-images.githubusercontent.com/68082746/172725066-ba404db3-63db-4053-97e4-049705faff5a.png)

- Allowing access from anywhere is *not a good security practice. Production clusters should not have this enabled and should limit network access.
- Finally, click Finish and Close at the bottom.

#### Load the Sample Dataset

- Select the "…" option in the cluster menu -> choose the "Load Sample Dataset" option, then confirm your choice.

![image](https://user-images.githubusercontent.com/68082746/172725164-8f2ba10b-49da-43fb-8d09-de73544a6a64.png)
![image](https://user-images.githubusercontent.com/68082746/172725181-ecb10064-244e-4301-8154-65b0b1d136dc.png)

- When the dataset is loaded the graph labeled "Logical Size" on the right side of the screen should go up and display the size of the dataset that is above zero and below 512 MB. Your graph may look different than the picture below.

![image](https://user-images.githubusercontent.com/68082746/172725211-80d66016-9d49-4871-934d-16585755fa70.png)
