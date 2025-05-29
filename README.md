# mongoDB-1
<pre>
  show dbs
admin     40.00 KiB
config   108.00 KiB
library   72.00 KiB
local     40.00 KiB
use todoapp
switched to db todoapp
db.todo.insertOne({})
{
  acknowledged: true,
  insertedId: ObjectId('6836e0ac2fa3675ffe5d0ebc')
}
db.todo.insertOne({ tasktodo:"go for grocery shopping"},{time:new Date()})
{
  acknowledged: true,
  insertedId: ObjectId('6836e20f2fa3675ffe5d0ebd')
}
db.todo.insertMany([{ tasktodo:"go for grocery shopping"},{time:new Date()},])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e2692fa3675ffe5d0ebe'),
    '1': ObjectId('6836e2692fa3675ffe5d0ebf')
  }
}
                                                                        
// Insert multiple books
db.books.insertMany([
  {
    tasktodo:"go to grocery shopping",
    time: new Date(),
    status:completed
  },
  {
    tasktodo: "study mongoDB",
    time: new Date("2023-01-15T10:00:00Z"),
    status: incomplete
  },
  {
    tasktodo: "study terraform",
    time: new Date("2023-01-15T10:00:00Z")
  })
// Insert multiple books
db.books.insertMany([
  {
    tasktodo:"go to grocery shopping",
    time: new Date(),
    status:completed
  },
  {
    tasktodo: "study mongoDB",
    time: new Date("2023-01-15T10:00:00Z"),
    status: incomplete
  },
  {
    tasktodo: "study terraform",
    time: new Date("2023-01-15T10:00:00Z"),status: incomplete
  },
  {
    tasktodo: "go home",
    status: incomplete
  },
])

// Insert multiple books
db.books.insertMany([
  {
    tasktodo:"go to grocery shopping",
    time: new Date(),
    status:completed
  },
  {
    tasktodo: "study mongoDB",
    time: new Date("2023-01-15T10:00:00Z"),
    status: incomplete
  },
  {
    tasktodo: "study terraform",
    time: new Date("2023-01-15T10:00:00Z"),status: incomplete
  },
  {
    tasktodo: "go home",
    status: incomplete,
  },
])
ReferenceError: completed is not defined
// Insert multiple books
db.books.insertMany([
  {
    tasktodo:"go to grocery shopping",
    status:completed
  },
  {
    tasktodo: "study mongoDB",
    time: new Date("2023-01-15T10:00:00Z"),
    status: incomplete
  },
  {
    tasktodo: "study terraform",
    time: new Date("2023-01-15T10:00:00Z"),status: incomplete
  },
  {
    tasktodo: "go home",
    status: incomplete
  }
])
ReferenceError: completed is not defined
// Insert multiple books
db.books.insertMany([
  {
    tasktodo:"go to grocery shopping",
    status:"completed"
  },
  {
    tasktodo: "study mongoDB",
    time: new Date("2023-01-15T10:00:00Z"),
    status: "incomplete"
  },
  {
    tasktodo: "study terraform",
    time: new Date("2023-01-15T10:00:00Z"),status: "incomplete"
  },
  {
    tasktodo: "go home",
    status: "incomplete"
  }
])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e4ea2fa3675ffe5d0ec0'),
    '1': ObjectId('6836e4ea2fa3675ffe5d0ec1'),
    '2': ObjectId('6836e4ea2fa3675ffe5d0ec2'),
    '3': ObjectId('6836e4ea2fa3675ffe5d0ec3')
  }
}
// Insert multiple books
db.books.insertMany([
  {
    tasktodo:"buy bag",
    status:"incomplete"
  },
  {
    tasktodo: "learn sql",
    status: "complete"
  },
  {
    tasktodo: "go to temple",
    status: "incomplete"
  },
  {
    tasktodo: "clock in",
    status: "complete"
  },
])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e5522fa3675ffe5d0ec4'),
    '1': ObjectId('6836e5522fa3675ffe5d0ec5'),
    '2': ObjectId('6836e5522fa3675ffe5d0ec6'),
    '3': ObjectId('6836e5522fa3675ffe5d0ec7')
  }
}
// Insert multiple books
db.books.insertMany([
  {
    tasktodo:"clockout",
    status:"incomplete"
  },
  {
    tasktodo: "submit docs",
    status: "complete"
  }
])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e5772fa3675ffe5d0ec8'),
    '1': ObjectId('6836e5772fa3675ffe5d0ec9')
  }
}
db.books.updateOne(
  { status: "completed" },                      
  { $set: { status: true } } 
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.books.updateOne(
  { status: "incomplet" },                      
  { $set: { status: false } } 
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.books.updateMany(
  { status: "incomplete" },                      
  { $set: { status: false } } 
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 6,
  modifiedCount: 6,
  upsertedCount: 0
}
db.books.updateMany(
  { status: "complete" },                      
  { $set: { status: true } } 
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 3,
  modifiedCount: 3,
  upsertedCount: 0
}
db.books.find({})
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec0'),
  tasktodo: 'go to grocery shopping',
  status: true
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec1'),
  tasktodo: 'study mongoDB',
  time: 2023-01-15T10:00:00.000Z,
  status: false
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec2'),
  tasktodo: 'study terraform',
  time: 2023-01-15T10:00:00.000Z,
  status: false
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec3'),
  tasktodo: 'go home',
  status: false
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec4'),
  tasktodo: 'buy bag',
  status: false
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec5'),
  tasktodo: 'learn sql',
  status: true
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec6'),
  tasktodo: 'go to temple',
  status: false
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec7'),
  tasktodo: 'clock in',
  status: true
}
{
  _id: ObjectId('6836e5772fa3675ffe5d0ec8'),
  tasktodo: 'clockout',
  status: false
}
{
  _id: ObjectId('6836e5772fa3675ffe5d0ec9'),
  tasktodo: 'submit docs',
  status: true
}
db.tasks.insertOne({
  title: "Learn MongoDB and terraform",
  isArchived: false,
  createdAt: new Date()
});
{
  acknowledged: true,
  insertedId: ObjectId('6836e8da2fa3675ffe5d0eca')
}
db.books.insertOne({
  title: "Learn MongoDB and terraform",
  isArchived: false,
  createdAt: new Date()
});
{
  acknowledged: true,
  insertedId: ObjectId('6836e91c2fa3675ffe5d0ecb')
}
db.books.insertOne({})
{
  acknowledged: true,
  insertedId: ObjectId('6836e9e22fa3675ffe5d0ecc')
}
db.books.insertOne({status:{$exists:false}},{$set:{status:false}})
{
  acknowledged: true,
  insertedId: ObjectId('6836ea512fa3675ffe5d0ecd')
}

db.books.updateMany(
  { status: { $exists: false } },  
  { $set: { status: false } }     
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 2,
  modifiedCount: 2,
  upsertedCount: 0
}
db.tasks.updateOne(
  { tasktodo:"go home" },
  { $set: { priority: "medium" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.tasks.updateMany(
  { tasktodo: "go home", priority: { $exists: false } },
  { $set: { priority: "high" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.books.updateMany(
  { priority: { $exists: false }, tasktodo: { $in: ["go to grocery shopping", "go home"] } },
  { $set: { priority: "low" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 2,
  modifiedCount: 2,
  upsertedCount: 0
}
db.books.updateMany(
  { priority: { $exists: false }, tasktodo: { $in: ["study terraform", "study mongo"] } },
  { $set: { priority: "high" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.books.updateMany(
  { priority: { $exists: true }, tasktodo: { $in: ["study terraform", "study mongo"] } },
  { $set: { priority: "high" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 0,
  upsertedCount: 0
}
db.books.updateMany(
  { priority: { $exists: false }, tasktodo: { $in: ["study terraform", "study mongoDB"] } },
  { $set: { priority: "high" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.books.insertOne({})
{
  acknowledged: true,
  insertedId: ObjectId('6836efdd2fa3675ffe5d0ece')
}
db.books.insertOne({
tasktodo:"go home",status:false})
{
  acknowledged: true,
  insertedId: ObjectId('6836f0192fa3675ffe5d0ecf')
}
db.books.updateOne({
tasktodo:"go home"},{$set:{Updatedat:new Date()}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.books._id({})
TypeError: db.books._id is not a function
db.books.countDocuments({})
15
db.tasks.find().sort({ priority: 1 })
db.books.find().sort({ priority: 1 })
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec4'),
  tasktodo: 'buy bag',
  status: false
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec5'),
  tasktodo: 'learn sql',
  status: true
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec6'),
  tasktodo: 'go to temple',
  status: false
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec7'),
  tasktodo: 'clock in',
  status: true
}
{
  _id: ObjectId('6836e5772fa3675ffe5d0ec8'),
  tasktodo: 'clockout',
  status: false
}
{
  _id: ObjectId('6836e5772fa3675ffe5d0ec9'),
  tasktodo: 'submit docs',
  status: true
}
{
  _id: ObjectId('6836e91c2fa3675ffe5d0ecb'),
  title: 'Learn MongoDB and terraform',
  isArchived: false,
  createdAt: 2025-05-28T10:44:44.630Z,
  status: false
}
{
  _id: ObjectId('6836e9e22fa3675ffe5d0ecc'),
  status: false
}
{
  _id: ObjectId('6836ea512fa3675ffe5d0ecd'),
  status: {
    '$exists': false
  }
}
{
  _id: ObjectId('6836efdd2fa3675ffe5d0ece')
}
{
  _id: ObjectId('6836f0192fa3675ffe5d0ecf'),
  tasktodo: 'go home',
  status: false
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec1'),
  tasktodo: 'study mongoDB',
  time: 2023-01-15T10:00:00.000Z,
  status: false,
  priority: 'high'
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec2'),
  tasktodo: 'study terraform',
  time: 2023-01-15T10:00:00.000Z,
  status: false,
  priority: 'high'
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec0'),
  tasktodo: 'go to grocery shopping',
  status: true,
  priority: 'low'
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec3'),
  tasktodo: 'go home',
  status: false,
  priority: 'low',
  Updatedat: 2025-05-28T11:16:39.772Z
}
db.books.updateMany(
  { status: false, dueDate: { $exists: false } },
  { $set: { dueDate: new Date() } }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.books.find({})
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec0'),
  tasktodo: 'go to grocery shopping',
  status: true,
  priority: 'low'
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec1'),
  tasktodo: 'study mongoDB',
  time: 2023-01-15T10:00:00.000Z,
  status: false,
  priority: 'high',
  dueDate: 2025-05-28T11:22:41.032Z
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec2'),
  tasktodo: 'study terraform',
  time: 2023-01-15T10:00:00.000Z,
  status: false,
  priority: 'high',
  dueDate: 2025-05-28T11:22:41.032Z
}
{
  _id: ObjectId('6836e4ea2fa3675ffe5d0ec3'),
  tasktodo: 'go home',
  status: false,
  priority: 'low',
  Updatedat: 2025-05-28T11:16:39.772Z,
  dueDate: 2025-05-28T11:22:41.032Z
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec4'),
  tasktodo: 'buy bag',
  status: false,
  dueDate: 2025-05-28T11:22:41.032Z
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec5'),
  tasktodo: 'learn sql',
  status: true
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec6'),
  tasktodo: 'go to temple',
  status: false,
  dueDate: 2025-05-28T11:22:41.032Z
}
{
  _id: ObjectId('6836e5522fa3675ffe5d0ec7'),
  tasktodo: 'clock in',
  status: true
}
{
  _id: ObjectId('6836e5772fa3675ffe5d0ec8'),
  tasktodo: 'clockout',
  status: false,
  dueDate: 2025-05-28T11:22:41.032Z
}
{
  _id: ObjectId('6836e5772fa3675ffe5d0ec9'),
  tasktodo: 'submit docs',
  status: true
}
{
  _id: ObjectId('6836e91c2fa3675ffe5d0ecb'),
  title: 'Learn MongoDB and terraform',
  isArchived: false,
  createdAt: 2025-05-28T10:44:44.630Z,
  status: false,
  dueDate: 2025-05-28T11:22:41.032Z
}
{
  _id: ObjectId('6836e9e22fa3675ffe5d0ecc'),
  status: false,
  dueDate: 2025-05-28T11:22:41.032Z
}
{
  _id: ObjectId('6836ea512fa3675ffe5d0ecd'),
  status: {
    '$exists': false
  }
}
{
  _id: ObjectId('6836efdd2fa3675ffe5d0ece')
}
{
  _id: ObjectId('6836f0192fa3675ffe5d0ecf'),
  tasktodo: 'go home',
  status: false,
  dueDate: 2025-05-28T11:22:41.032Z
}
todoapp


</pre>
