#### Partition Keys

    A partition is an allocation of storage for a table.
    Adaptative Capcity shared capacity maximum 3000 RCU and 1000WCU per partition.
    Using cache layer DAX.

##### Best Practices

    - A good partitioning scheme affords even distribution of both data and workload, with growth in mind.
    - Think of partition key as the dimension of scalibility and distribute aggregates accros parititions
    - Ideal scaling conditions
        * Partition key is from a highh cardinality set
        * Requests are evenly spread over the key space
        * Requests are evenly spread over time

