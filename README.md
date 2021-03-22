# Mongo note

brew services start mongodb-community
Mongo data types: Boolean, Null, Interger, Double, String, BigInt, Object, Array, Symbol, Date, Object ID
mongo command:
  - show dbs; list databases.
  - use <db-name>; select, create a database.
  - db;
  - db.<collection>; create a collection.
	db.<collection>.insert({})
  - db.getCollectionNames(); show all collection.
  - db.<collection name>.find(query); show document in collection.
	{key: value}
	{key: {$ne: value}} not equal
	{key: {$gt: value}} greater than
	{key: {$gte: value}} greater than equal
	{key: {$lt: value}} less than
	{key: {$lte: value}} less than equal
	{key: {$in: values}} 
	{key: {$nin: values}} not in
  - $and: 
	db.<collection>.find({
	  key1: value1,
	  key2: value2
	})
   -  $or:
	db:collection.find({
	  $or: [condition1, condition2]
	});
  - $where: 
	db.collection.find({ $where: "javascript expression" })
	db.user.find({ $where: "this.first_name === 'aaa'" })
  - pagination:
	db.<collection name>.find(query).skip(6).limit(6)
  - sort: 
	db.collection.find(query).sort({field: -1})
	field: 1: ascending order
	field: -1: descending order
  - CRUD: 
	db.collection.insert(doc);
	db.collection.insertMany(docs);
	db.collection.find(query);
	db.collection.findOne(query);
	db.collection.updateOne(query, data);
	db.collection.updateMany(query, data);
	db.collection.deleteOne(query);
	db.collection.deleteMany(query);
  - operators: $inc(increase), $push, $pull, $addToSet
  - collection methods: 
	db.collection.drop();
	db.collection.renameCollection(<new name>);
