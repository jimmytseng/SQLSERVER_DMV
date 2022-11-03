## Type of index
##### Clustered
叢集索引將資料表的資料列依其索引鍵值排序與儲存。
如果資料表沒有任何叢集索引，它的資料列就儲存在未排序的結構中，這個結構稱為堆積。
##### Nonclustered
非叢集索引有一個與資料列完全分開的結構。 非叢集索引包含非叢集索引鍵值，而每個索引鍵值項目都有一個指標，指向包含索引鍵值的資料列。
##### Covered
包含所有欄位 
##### Composite
包含部分欄位


## Types of index access
##### Seek
查詢條件包含Index組成的第一個欄位
##### Scan
查詢條件包含Index的組成欄位
##### Lookup
SELECT要求Index未包含的欄位，則還需透過Key Lookup找到資料列讀取資料

## Factors affecting index performance
##### FILL FACTOR
SQL SERVER 預設 Fill Factor為0-100，如果設定太低，如只設定20，則會造成浪費空間，每一個page只有30%的空間，會造成資料散佈的問題與浪費儲存空間。
 
##### FRAGMENTATION
Index存放到Page的資料可能在更新後，造成資料產生內部碎裂或外部碎裂。
