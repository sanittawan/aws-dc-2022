## Designing a data mesh architecture using AWS Lake Formation and AWS Glue
trainer: Tonny Ouma

**business needs**
- main problem is data are in silo. Data can be kept in different data lakes
- diverse consumers of data
- need self-service
- privacy and compliance - data not ending up in the wrong hands
- need secured collab and sharing

**modern data architecture**
- it's a repository and store them in raw format (store as is)
- e.g. images stored as is in S3

**data lakes**
- data lake is flexible and doesn't require a fixed format (like relational, non-relation, warehousing etc.)
- each object can communicate with each other
- data in the data lakes should be mutable and have lineage (version)
- but to make this work, you need central governance

**data mesh**
- data lake brings all data into a common repository, but business needs to be quick. Data Scientists need the data. 
- Data mesh is a pattern and comes to help with this problem of everything is in a lake
- idea is the distributed control
- in the developer realm, it's microservices. data mesh is like microservices
- data producers are really good at producing the data and provide API to access the data. They serve data products instead of microservices
- at the end of the day, data mesh is a collection of data lakes
- it's based on domain specific, rather than having everything in one place. The idea is that you have many domain-specific data lakes. E.g. Stateform, home insurance has their own data lake and auto-insurance has their own data lake
- federating --> pointing to the data in autoinsurance. But they must share a common tech stack. You don't copy the data. 
- data mesh = Glue and Lake Formation 
- data mesh, the producer publishes the data to the mesh and the consumers come in and grab it  
- e.g. bank account published by one producer is not the same as client account by another. Consumers can choose what "account" they need

**AWS**
- S3 for storage 
- Lake Formation is the key to data mesh
- AWS Glue is the data catalog which stores metadata about the underlying data 
- ETL should be done with the data producers, not in the mesh
- producer can be a consumer in the domain of which he is not an expert
