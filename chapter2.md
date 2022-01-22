#### Understanding DynamoDB Data Structures


- NoSql - Schema on Read.
Allow arbitrary data in the collection.

##### DynamoDb and Table

- Consistent, predictable perfomance
- Single-digit milliseconds latency
- Both wide column and key-value store.

- ReadCapacityUnit
 
  - 1 RCU =  1 strong consistend read up to 4KB
  - 1 RCU = 2 eventual consisten up to 4 kb.
  - 2 RCU = 1 transactional read/sec up to 4 KB.
  
- WriteCapacityUnit

    - 1 WCU = 1 standard wirte/sec up to 1kb
    - 2 WCU = 1 transactional write/sec up to 1kb


##### Items and Attributes

- Items are uniquely identifiable by a primary key, set at table creation time
- Max item size:400kb

