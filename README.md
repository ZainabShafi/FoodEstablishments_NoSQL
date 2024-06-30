# UK FOOD STANDARDS AGENCY ANALYSIS: 

For my first foray into utilizing and querying MongoDB or non-SQL/non-relational databases, I was tasked with analyzing UK Food Standard Agency ratings data on various public establishments and querying it through Pymongo. This assignment solidified basic Pymongo/MonoDB(shell and compass) query structures, and covered basic CRUD (Create, Read, Update, Delete) operations through Pymongo; including data importation into MongoDB, to aggregate queries and operators.

## Technologies Used: 

MongoDB: MongoDB is a NoSQL database that is used for storing and managing the food establishment data. It provides flexibility in schema design and scalability for handling large volumes of data.

*PyMongo* : MongoDB Driver for Python - Python: PyMongo is a Python library that makes it easy to write scripts, manipulate data, and develop applications.
MongoDB: PyMongo works with MongoDB, a NoSQL database that is flexible, scalable, and stores data in documents.
BSON (Binary JSON): PyMongo uses BSON to exchange data between Python and MongoDB. BSON is like JSON but includes more data types and is efficient in storage and speed.

Pandas: Utilized for data manipulation and aggregations (primarily for dataframe creation and inspection). 

MongoDB Compass: MongoDB Compass, although not directly mentioned in the project, is a graphical user interface (GUI) tool for MongoDB. It allowed for visual exploration and manipulation of the MongoDB database. 

## Coding Logic: 

**NoSQL_setup:**

This notebook is to be run first, it contains code for importing the food establishments data (establishments.json) in the "Resources" folder to MongoDB for further organization and cleaning. The code proceeds to follow CRUD operations: 

1) *Creates* and 'uk_food' database through JSON specific mongoimport code.
2) *Read* : Connects and names the 'establishment' collection, and executes .find query. 
3) *Updates* the database with a new restaurant record, and modifies other aspects of the database such as changing data types.
4) *Deletes* records with certain criteria 

**NoSQL_analysis:** 

This notebook contains more complex aggregation queries using pymongo, specifically utilizing MongoDBs aggregation pipeline. The results of this queries are then displayed as Pandas data frames. Key query operators include: 

1) *count_documents* to fetch the number of documents within certain parameters (for eg., establishments with a hygiene score of 20).
2) *regex* to fetch establishments in a certain locale that contain a phrase.
3) *sort* to order documents returned by query based on one or more fields.
4) *match* includes documents in results that match parameters set by query.
5) *groups* documents by a specified field and can perform operations such as counting, summing, averaging, etc., within each group. It creates a new set of documents, each representing a group.

Aggregation Pipeline eg:
<img width="915" alt="Screenshot 2024-06-30 at 12 52 03 AM" src="https://github.com/ZainabShafi/FoodEstablishments_NoSQL/assets/160359466/e0775dd1-7b31-47b9-987a-bdc76d245e73">
