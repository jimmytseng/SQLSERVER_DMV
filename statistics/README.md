 Statistics are created automatically for indexes. In addition, when the optimizer 
comes across a column that¡¦s used in a JOIN condition or a WHERE clause, and no 
index exists, the optimizer will usually create statistics on the column. There are conditions that prevent statistics from being created or updated, and we¡¦ll discuss these 
later in this section. Sometimes, non-index-related statistics, including missing statistics, are indicators of missing indexes, and inspecting the DMVs that reveal missing 
indexes should confirm this. 