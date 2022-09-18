What is LINQ?
    LINQ stands for Language Integrated Query. It’s a method for querying data used in a .NET platform 
    that is similar to the SQL query. LINQ can query any type of data, be it a set of objects, database or XML files.
    
    LINQ will work on any collection class that gears the IEnumerable interface

What are the types of LINQ?
    LINQ to Objects
    LINQ to XML
    LINQ to Dataset
    LINQ to SQL
    LINQ to Entities

LINQ is useful than Stored Procedures
    Debugging: It is difficult to debug a stored procedure but as LINQ is part of.NET, visual studios debugger can be used to debug the queries
    Deployment: For stored procedure, additional script should be provided but with LINQ everything gets compiled into single DLL hence deployment becomes easy
    Type Safety: LINQ is type safe, so queries errors are type checked at compile time


Query and Sequence operators in LINQ
    The sequence is a collection class on which you want to query
    Query operators take in the sequence as input, process it and return the new result sequence.

Lambda expressions in LINQ?
    Lambda expression is referred as a unique function use to form delegates or expression tree types, where right side is the output and left side is the input to the method.


 Skip() and SkipWhile()
    Skip=> It will take an integer argument and from the given IEnumerable it skips the top n numbers
    SkipWhile()=>It will continue to skip the elements as far as the input condition is true

DataContext classes in LINQ
    DataContext class acts as a bridge between SQL Server database and the LINQ to SQL