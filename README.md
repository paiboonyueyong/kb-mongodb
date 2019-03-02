# kb-mongodb

Compare Sql and Nosql

      Table = Collection

      Row = Document

      Column = Field

# mongodb command

Point to database current use
   
    use contactchain_db

Create collection (Table)

      db.createCollection("contact")'

Show all database

      show dbs

Show all collection in database

      show collections

Drop database current use

      db.dropDatabase()
      
Create collection employees and insert data

      db.employees.insert(
          {
           "FirstName":"Paiboon Yuenyong",
           "Tel":"0864126585",
           "Email":"paiboon@simple.com",
           "Salary":1000000
          }
      )
      
Change database name >> change mydb to sale_prediction

    db.copyDatabase("mydb","sale_prediction")
    use mydb
    db.dropDatabase();
    
Delete single document from collection by _id

    db.[collection_name].deleteOne({"_id" : ObjectId("5b4d763957c44232e0685e7d")});
    
Delete field from collection multi ducument
    
      db.[collection_name].update({}, {$unset: {OBJECTID: 1}}, {multi: true})
      
Delete multi field from collection multi ducument

      db.FishNet.update({}, {$unset: {
                                "Join_Count" : "1",
                                "TARGET_FID" : "1",
                                "JOIN_FID" : "1",
                                "Shape_Length" : "1",
                                "Shape_Area" : "1"
                                }
                       }, {multi: true})
                       
## How do you query this in Mongo? (is not null)

Given these inserts:

      db.test.insert({"num":1, "check":"check value"});
      db.test.insert({"num":2, "check":null});
      db.test.insert({"num":3});
      
This will return all three documents:

      db.test.find();

This will return the first and second documents only:

      db.test.find({"check":{$exists:true}});

This will return the first document only:

      db.test.find({"check":{$ne:null}});

This will return the second and third documents only:

      db.test.find({"check":null})

## Convert Data Type

      db.[collection name].find({[field name]: {$exists:true}}).forEach( function(x) {
          db.[collection name].update({_id: x._id}, {$set: {[field name]: x.[field name].toString()}});
      });
     

## Enable Authentication

      Link >> https://medium.com/mongoaudit/how-to-enable-authentication-on-mongodb-b9e8a924efac
      
## Tutorial
      
      https://www.tutorialspoint.com/mongodb/index.htm







