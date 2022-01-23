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



##### Partitions and Sort Keys

- Partition key/hash key
- Sort key/range

Combination must be unique

##### Data types

Scalar: number,string, binary, boolean and null
timestamp in epoch time (numbers of seconds)

Document:
list and map

Set: multiple scalar values of same types.
no ordering/ not empty set

#### Indexes

Secondary indexes are data structures that contain a subset of attributes from
a table, along with an alternate key to support query operations.

Global Secondary Index( GSI): Index with a different
partition and sort key from those on the base table.
The primary key of a GSI can be either
simple or composite

Local Secondary Index(LSI) Index that has the
same partition key as the base table,
but a different sort key. The primary key
of an LSI must be composite. It must be created
at the time of table creation.

GSI: Eventually consistent only
LSI strongly or eventual consistent query

