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

or 

db.messages_copy.aggregate([
    {"$group" : {_id:"$processid", count:{$sum:1}}},
    { "$sort": { count: -1 } }
])

```


**copy one collectin to another ** in $match is where condition
```js
db.messages.aggregate([ { $match: {  } }, { $out: "messages_copy" } ]);
```

**Update Many**
```js
db.messages_copy.updateMany(
        {
                processid: "FC3A87A1-61FC-4DA0-BFAB-2541C6ADDFD7"
        }, 
        { 
                $set: { inElastic: false} 
        })
```
