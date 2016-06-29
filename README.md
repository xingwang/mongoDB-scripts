# mongoDB-scripts
Useful mongoDB scripts

## Batch update/insertion
Update operators reference [here](https://docs.mongodb.com/manual/reference/operator/update/)
```js
db.<collection>.find().forEach( 
function(item)
{  
  db.<collection>.update({_id: item._id}, {$push:{"keywords": "super monkey"}},false, true);
});
```
