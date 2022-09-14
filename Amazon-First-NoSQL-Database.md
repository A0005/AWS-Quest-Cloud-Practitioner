1 - Amazon DynamoDB:

    Amazon DynamoDB is serverless with no servers to provision, patch, or manage and 
    no software to install, maintain, or operate. Amazon DynamoDB automatically 
    scales tables up and down to adjust for capacity and maintain performance.
    
    Amazon DynamoDB supports both key-vaule and document data models. This enables
    Amazon DynamoDB to have a flexible schema, so each row can have any number
    of columns at any point in time. This allows you to easily adapt the tables
    as your business requirements change, without having to redefine the table
    schema as you would in relational databases.
    
    When you create a table, in addition to the table name, you must specify 
    the primary key of the table. The primary key uniquely identifies each item 
    in the table, so that no two items can have the same key.
    
    A composite key. uses both a partition key and a sort key. In a table that has
    a partition key and a sort key, its possible for two items to have the same
    partition key value. However, those two items must have different sort key vaules.
    
    With, Amazon DynamoDB you create items, which are records with attributes 
    that store data. You can store data like a customer's video viewing history.
    Amazon DynamoDB supports a number of different data types.
    
    Amazon DynamoDB can also store attributes that are more complex such as a list.
    
    After you've created a record you can still edit it. That includes the contents
    of the record and its attributes.
    
    Amazon DynamoDB is schemaless, meaning you can add attributes to the table for any record.
    You can add a lastStopTime attribute with a Number data type that stores the total time
    in seconds for video viewing. This data could be leveraged for a resume feature in your
    application.
    
    The Query operation in Amazon DynamoDb finds items based on primary vaules.
    You must provide key the name of the partition key attribute and a single
    vaule for that attribute. The queery returns all items with that partition
    key vaule. Optionally, you can provide a sort key attribute and use a comparison
    operator to refine the search results.
    
    When running a Query operation the table looks for an excat match for the
    partition key and uses the sort key (if provided) as way to futher limit
    the results.
    
    The Scan operation returns one or more items and item attributes by accessing 
    every item in a table or a secondary index. If the total number of scanned items.
    If the total number of scanned items exceeds the maximum dataset size limit of 1 MB,
    the scan stops and results are returned to the user as a LastEvaluatedKey value, to
    continue the scan in a subsequent operation. The results also include the number
    of items exceeding the limit. A scan result in no table data meeting the filter criteria.
    
    
    
    
    
    
    
    
    
    
    
    
    
