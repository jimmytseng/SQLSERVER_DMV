##Phenomena 
#####--lost update
兩個交易以上對同一欄未更新時，未對欄位進行鎖定。則可能造成交易被覆蓋的結果。
#####--Dirty Read
可能讀取到其他transaction未commit的資料，rollback資料後造成資料錯誤。
#####--Non-repeatable Read
在同一個 Transaction 中，重複讀取時會拿到不一致的資料。
#####--Phantom Read
交易中有另一個交易新增或刪除資料，造成第二次查詢多了資料或少了資料。

##Isolation levels 隔離等級
#####--Read Uncommitted 
允許讀取未Commit的資料，有可能發生DirtyRead，可避免lost update。
#####--Read Committed 
讀取已Commit的資料，可避免DirtyRead。
#####--Repeatable Read 
同一筆交易中讀取的資料必須相同，至少可避免 unrepeatable read 。
#####--Serializable Isolation
交易必須可以循序，會造成重大效能問題。





