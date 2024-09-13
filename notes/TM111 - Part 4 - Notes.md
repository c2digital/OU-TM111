---
title: TM111 - Part 4 - Notes
created: '2024-09-12T07:51:26.512Z'
modified: '2024-09-13T08:00:47.678Z'
---

# TM111 - Part 4 - Notes

** =** 
**Attribute =** properties describing an entity
**Data =** One or more values that can be assigned to an object. It can assume any form (numbers, letters, pictures etc) but has no context. "100meters" is data but means nothing without the context.
**Database =** A collection of related data stored in an organised manner for efficent reading and updating
**Entity =** an item about which we want to store data. Can be tangible (a person, building etc) or intagible (an event, study objective). Described using attributes.
**Instance =** an instance of an entity. Whereas an entity could be 'student', the instance would be the object 'Carl Mason' of the student type.
**Normalisation =** dividing data in a database into two or more tables with relationships
**Query Language =** combines limited set of english phrases with logical commands. SQL is the most propular.


## Notes
- Data on its own has no context. Data is turned into useful information by placing it within context.
- Computer programs process data following instructions.
- When we want to store large amounts of data, we use a database

### Flat Databases
- Simpliest of all, also known as just a table
- Column = field. Row = record.
- Interact with the database using queries
- Becomes cumberson when adding new fields and updated selected rows, as well as requiring duplicating data. 

### Relational Databases
- Overcomes the problems of flat databases
- Divides data into two or more tables (known as normalisation). The benefits of normalisation includes:-
  - It is not necessary to have empty fields as with the flat table as many relations can be created in a joining table
  - If a change is required, it only has to be made in one table/row, rather than duplicating across many rows
  - No more unneccesary repetition
- Uses entities and instances of entities
- Entities have attributes (such as date of birth). Instances have values of intributes (such as 7th April 1989).
- Relationships are stored in 'joining tables' Such as a student_id to a course_id.
- Joining tables are for the convenience of the computer, not that user friendly to humans
- Relationships can be one-to-many, many-to-many and many-to-one

### Views

- Databases permit 'views' - which uses a query to combine data from one or more tables to create virtual tables, which can be queried itself
- Views are useful for:-
  - Showing table from multiple tables together
  - Limiting access to data (eg. retrieve a users basic profile without contact details)
  - Combining data from tables based on criteria
  - Can be assigned as 'readonly' to prevent unwanted access/changes
- On the downside:-
  - Depend on the arrangement of the underlying tables. If the table structures are changed, the views need updating too
  - Data access is slightly slower

### Database Management Systems (DBMS)

- MSSQL, IBM DB2, MySQL etc
