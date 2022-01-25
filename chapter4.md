##### Common Patterns

    Design tables to optimize for your applications access patterns
    Identify access patterns by;
     * New apps - review users stories and analyze the candidate access patterns
     * Existing apps - analyze logs

    Example key access patterns:
    FInd employee by ID
    Get all items for a given order ID
    Get all employee for a department
   
    Optimize for the most common  querie's speed and cost
    Use a few tables as posibble

    Single table design helps avoids:
       - N+1 problem, 
       - Using or abusing transaction apis
       - Higher latency to the end user.
       - More complexity per query
       - Much higher costs

#### One to Many relationships

    SK= different sort key
    FOr oders for example:
    OrderId: PK
    SK: order:item1
        shipTO

#### Adjency list - Many to Many Relationships

    Employess
    Employees_projects
    Projects

    Business Questions:
    TO which projects does Employ X belong
    Which employees are assigned to projects y
    Model our data using the adjancey list pattern  
    Use an overlloaded GSI partition key
    
      PK                  SK             first_name                  last_name
    Projects1          Projects1
                       Employee1
                       Employee2

    Employee1          Employee1           John                       Pornoy


##### Hierarchical Data

    Hierarchical OLTP, USIN PRE-COMPUTED KEY,
    inidicates we create sort key with value from the partition key, to be used with some operators in query 
    

    
    
