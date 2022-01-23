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

   
    
