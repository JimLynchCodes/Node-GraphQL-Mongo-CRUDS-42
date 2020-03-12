# Node GraphQL Mongo CRUDS 42


CRUDS is an acronym that stands for "create, read, upadate, delete, subscribe". This is an example of a contrived, especially simple data to keep things simple.

### Specs for the "42 Server"
The business needs to keep records of the number 42 (don't ask us why, they just really need it!). 

Records in this case are documents, the top level objects of a mongo database collection.

For our business, a record **must** have one single (not counting inherent ones such as \_id) key that is the string "record", and it **must** be created with the value 42. It is able to be updated, but can _only_ be updated to the value 43 and afterwords may not be updated again!

Thus, all the records are objects that look like this:
```
{ record: 42 }
```

High level spec: We need a GraphQL endpoint for each of the following operations:

### C - Create
- insert a new record

### R - Read
- read an individual record by \_id
- reads all records (full list)
- reads all records (cursor pagination)

### U - Update
- update a record by \_id from 42 to 43 

### D - Delete
- delete a record by \_id

### S - Subscribe
- subscribe to a changelog of records being added, updated, and deleted.


