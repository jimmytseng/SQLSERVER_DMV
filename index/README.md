## Type of index
##### Clustered
This index is the table itself with the physical order of the rows 
defined. It’s typically good for range-based queries.
##### Nonclustered
An index that contains a subset of a table’s columns. It’s typically 
good for retrieving a small subset of easily identified rows
##### Covered
An index that contains all the data required by a query. 
##### Composite
An index that’s composed of more than one column
##### Filtered
An index that’s based on a WHERE clause. This feature is present 
only in SQL Server 2008 and higher

## Types of index access
##### Seek
Selectively accesses discreet rows of data in an inde
##### Scan
Accesses a range of index rows 
##### Lookup
Selectively accesses discreet rows of data in index and then gets additional data from the index’s underlying table via a lookup

## Factors affecting index performance
##### FILL FACTOR
Fill factor describes how full an index page is.
Similarly, when you’re 
identifying a group of rows that are to be subsequently updated, you want to be able to 
obtain as much data as possible per read operation. But when you need to insert data, 
which needs to be placed in sequence with related data, the index page should contain space for this. When there’s no space in the index page, page splitting will occur, 
resulting in queries taking longer because lookups need to be performed.
Your dilemma is being able to balance the need for this additional space to cater 
for any inserts/updates with the need to retrieve as many rows as possible with each 
page read
a fill factor of 50% means reads are twice as 
slow as when the fill factor is 100. You must take care not to overstate the role of index 
updates in determining the index’s fill factor.
 
##### FRAGMENTATION
Logical index fragmentation describes the percentage of index entries that are out of sequence.
This has an impact on indexes that are involved in scans, increasing the amount of work they have to do because the index data isn’t contiguous.
