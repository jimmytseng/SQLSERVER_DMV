Isolation levels
--Read Uncommitted 
This causes SELECT statements to ignore most locks and not take out 
any locks.
--Read Committed 
This is the default isolation level. A query will wait until data has been committed or rolled back before SELECTing it.
--Repeatable Read 
Any locks caused by SELECTs are held until the end of the transaction.
Serializable Locks are taken out not only on the rows being selected/updated but also on nearby rows; 
this prevents the insertion of data that might affect the query. 
--Read Committed Snapshot
This relates to keeping a copy of any prechanged data, enabling better 
concurrency. Statement based.
--Snapshot 
This relates to keeping a copy of any prechanged data, enabling better 
concurrency. Transaction oriented