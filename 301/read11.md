# NoSQL vs SQL Databases
NoSQL (“non SQL” or “not only SQL”) databases were developed in the late 2000s with a focus on scaling, fast queries, allowing for frequent application changes, and making programming simpler for developers. Relational databases accessed with SQL (Structured Query Language) were developed in the 1970s with a focus on reducing data duplication as storage was much more costly than developer time. SQL databases tend to have rigid, complex, tabular schemas and typically require expensive vertical scaling.


|    | SQL    | noSQL    |
| ----------- | ----------- | ----------- |
|   Data Storage Model |  Tables with fixed rows and columns    |  Document: JSON documents, Key-value: key-value pairs, Wide-column: tables with rows and dynamic columns, Graph: nodes and edges    |
|   Development History |  Developed in the 1970s with a focus on reducing data duplication    |  Developed in the late 2000s with a focus on scaling and allowing for rapid application change driven by agile and DevOps practices.   |
|   Examples |  Oracle, MySQL, Microsoft SQL Server, and PostgreSQL  |  Document: MongoDB and CouchDB, Key-value: Redis and DynamoDB, Wide-column: Cassandra and HBase, Graph: Neo4j and Amazon Neptune   |
|   Primary Purpose |  General purpose    | Document: general purpose, Key-value: large amounts of data with simple lookup queries, Wide-column: large amounts of data with predictable query patterns, Graph: analyzing and traversing relationships between connected data  |
|   Schemas|  Rigid    |  Flexible    |
|   Scaling |  Vertical (scale-up with a larger server)    |  Horizontal (scale-out across commodity servers |
|  Multi-Record ACID Transactions |   Supported   |  Most do not support multi-record ACID transactions. However, some—like MongoDB—do.    |
|   Joins |  Typically required    | Typically not required    |
|   Data to Object Mapping | Requires ORM (object-relational mapping)   |  Many do not require ORMs. MongoDB documents map directly to data structures in most popular programming languages.    |


























