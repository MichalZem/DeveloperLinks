# MongoDb Snippets

**mongodb group by**
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

** copy one collectin to another ** in $match is where condition
```js
db.messages.aggregate([ { $match: {  } }, { $out: "messages_copy" } ]);
```
