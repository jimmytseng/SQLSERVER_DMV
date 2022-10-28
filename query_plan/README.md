## executed queries
When a SQL query is run for the first time, the optimizer has to determine an optimal 
way of satisfying the query. Typically, the optimizer looks at the record counts, available indexes, and statistics to determine the access paths necessary to fulfill the query 
easily and quickly. The optimizer takes time to do this work. Rather than having to 
perform this work for queries that are the same (except for different parameters), the 
optimizer creates a cached plan that describes the access mechanism. This plan can 
be reused by all subsequent similar queries.