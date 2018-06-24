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





