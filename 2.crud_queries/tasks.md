1. Create a database named `blog`.
   use blog

2. Create a collection called 'articles'.

3) Insert multiple documents(at least 3) into articles. It should have fields
   db.articles.insertMany([])

4. Find all the articles using `db.COLLECTION_NAME.find()`
   db.article.find()

5. Find a document using \_id field.
   db.article.find({\_id : ObjectId("5e3d0c1b5ba0842fd6bcd152")})

6) Find documents using title and author's name field.
   db.article.find({'author.name':"Bimlendu Kumar"})

7. Find doucment using a specific tag.
   db.article.find({tags: 'js'

8) Update title of a document using its \_id field.
   db.article.update({\_id : ObjectId("5e3d0c1b5ba0842fd6bcd152")},{\$set :{'author.name':'anas'}})

9. Update a author's name using article's title.
   db.article.update({title : 'css'},{\$set :{'author.name':'anas kumar'}})

10. Add additional tag in a specific document.
    db.article.update({title : 'css'},{\$set :{'author.name':'anas kumar'}}, {new:true})

11. Increment an auhtor's age by 5.
    db.article.update({title : 'css'},{\$inc :{'author.age':5}})

12) Delete a document using \_id field with `db.COLLECTION_NAME.remove()`.
    db.article.remove({\_id : ObjectId("5e3d0c1b5ba0842fd6bcd152")})
