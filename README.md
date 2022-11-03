# ** SQL SERVER DMV **
作者: Tseng Shang Hsuan ( Jimmy Tseng https://github.com/jimmytseng)

## 介紹
DMV 紀錄資料庫相關活動資訊，包括索引、查詢執行狀況、擴充活動、I/O等相關活動資訊。
利用這些資訊可以改善資料庫效能與維運使用。

##  DMV 資訊類別
##### --Change data capture 
為SQL Server 2008 以上可使用的功能，可記錄欄位、資料表與DDL相關變更等資訊，DML可記錄這些資訊
##### --Common Language Runtime
紀錄 SQL SERVER 執行的.NET程式相關資訊
##### --資料庫資訊統計
包含資料庫使用空間、分割(Partition)統計等
##### --鏡向功能 Database mirroring 
##### --Execution
包括執行計畫與查詢最佳化等資訊等
##### --Extended events
Extended Events 是一個意在取代SQL profiler效能監控工具，DMV可以記錄相關擴充事件的資訊
##### --全文檢索 Full-text search
##### --索引資訊 Index 
包含索引的統計與碎裂資訊
##### --Input/Output (I/O)
資料庫I/O read/write資訊
##### --查詢通知
##### --副本抄寫資訊 Replication
##### --Service Broker
藉以提供強固穩定的訊息平台
##### --SQL Server 作業系統
包含記憶體與系統相關資訊
##### --交易 Transaction
紀錄交易相關資訊包含snapshot, database, session, and locks.
##### --資料庫安全 Security


## 其他工具
##### SQL SERVER PROFILER
##### DATABASE TUNING ADVISOR
##### CACHED PLAN INSPECTION
