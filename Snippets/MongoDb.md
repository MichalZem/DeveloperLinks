# MongoDb Snippets

```js
db.getCollection('messages').aggregate([
{
        $group : {
           _id :{ $dateToString: { format: "%Y-%m-%d", date: "$Received"} },
           list: { $push: "$$ROOT" },
           count: { $sum: 1 }
        }
}
])
```