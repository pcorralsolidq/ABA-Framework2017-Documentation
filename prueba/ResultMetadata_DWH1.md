![](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif)

# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tablas](#head_tables)
  * [dim.author](#head_dim_author)
  * [dim.author$Changes](#head_dim_author_Changes)
  * [dim.newspapers](#head_dim_newspapers)
  * [dim.newspapers$Changes](#head_dim_newspapers_Changes)
  * [dim.publisher](#head_dim_publisher)
  * [dim.publisher$Changes](#head_dim_publisher_Changes)
  * [dim.store](#head_dim_store)
  * [dim.store$Changes](#head_dim_store_Changes)
  * [dim.title](#head_dim_title)
  * [dim.title$Changes](#head_dim_title_Changes)
  * [fact.sales](#head_fact_sales)
  * [fact.sales$Changes](#head_fact_sales_Changes)
  
* [Vistas](#head_vistas)
  

## Info {#head_info}
**ABA2017_DWH**

DB Info:

| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| ABA2017_DWH |     300.00 MB| sa| 7| Nov  2 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=869, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 140 |

Files:

| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| ABA2017_DWH_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_DWH_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| ABA2017_DWH_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_DWH_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| ABA2017_DWH_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_DWH_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tables

#### dim.author {#head_dim_author}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| author | dim | dbo | 02/11/2017 15:56:30 | 24 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_author | int | 4 | no |  | (n/a) |
| idauthor | varchar | 11 | yes | Modern_Spanish_CI_AS | no |
| au_lname | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| au_fname | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| phone | char | 12 | yes | Modern_Spanish_CI_AS | no |
| address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| contract | bit | 1 | yes |  | (n/a) |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| DWH | author | I | 02/11/2017 15:57:17 | 02/11/2017 15:57:20 | S | DESKTOP-HCA06TJ\Pablo Corral | 23 | 0 | 0 |

#### dim.author_Changes {#head_dim_author_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| author$Changes | dim | dbo | 02/11/2017 15:56:30 | 23 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_author | int | 4 | yes |  | (n/a) |
| idauthor | varchar | 11 | yes | Modern_Spanish_CI_AS | no |
| au_lname | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| au_fname | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| phone | char | 12 | yes | Modern_Spanish_CI_AS | no |
| address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| contract | bit | 1 | yes |  | (n/a) |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### dim.newspapers {#head_dim_newspapers}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers | dim | dbo | 02/11/2017 15:56:30 | 7 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_newspapers | int | 4 | no |  | (n/a) |
| idnewspapers | int | 4 | yes |  | (n/a) |
| name | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| DWH | newspapers | I | 02/11/2017 15:57:08 | 02/11/2017 15:57:09 | S | DESKTOP-HCA06TJ\Pablo Corral | 6 | 0 | 0 |
| stg | newspapers | I | 02/11/2017 15:51:51 | 02/11/2017 15:51:52 | S | DESKTOP-HCA06TJ\Pablo Corral | 6 | 0 | 0 |

#### dim.newspapers_Changes {#head_dim_newspapers_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers$Changes | dim | dbo | 02/11/2017 15:56:30 | 6 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_newspapers | int | 4 | yes |  | (n/a) |
| idnewspapers | int | 4 | yes |  | (n/a) |
| name | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### dim.publisher {#head_dim_publisher}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publisher | dim | dbo | 02/11/2017 15:56:30 | 9 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_publisher | int | 4 | no |  | (n/a) |
| idpublisher | char | 4 | yes | Modern_Spanish_CI_AS | no |
| pub_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| DWH | publisher | I | 02/11/2017 15:57:17 | 02/11/2017 15:57:20 | S | DESKTOP-HCA06TJ\Pablo Corral | 8 | 0 | 0 |

#### dim.publisher_Changes {#head_dim_publisher_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publisher$Changes | dim | dbo | 02/11/2017 15:56:30 | 8 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_publisher | int | 4 | yes |  | (n/a) |
| idpublisher | char | 4 | yes | Modern_Spanish_CI_AS | no |
| pub_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### dim.store {#head_dim_store}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| store | dim | dbo | 02/11/2017 15:56:30 | 7 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_store | int | 4 | no |  | (n/a) |
| idstore | char | 4 | yes | Modern_Spanish_CI_AS | no |
| stor_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| stor_address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| DWH | store | I | 02/11/2017 15:57:17 | 02/11/2017 15:57:20 | S | DESKTOP-HCA06TJ\Pablo Corral | 6 | 0 | 0 |

#### dim.store_Changes {#head_dim_store_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| store$Changes | dim | dbo | 02/11/2017 15:56:30 | 6 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_store | int | 4 | yes |  | (n/a) |
| idstore | char | 4 | yes | Modern_Spanish_CI_AS | no |
| stor_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| stor_address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### dim.title {#head_dim_title}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| title | dim | dbo | 02/11/2017 15:56:30 | 19 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_title | int | 4 | no |  | (n/a) |
| idtitle | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| title | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
| type | char | 12 | yes | Modern_Spanish_CI_AS | no |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| price | money | 8 | yes |  | (n/a) |
| advance | money | 8 | yes |  | (n/a) |
| royalty | int | 4 | yes |  | (n/a) |
| ytd_sales | int | 4 | yes |  | (n/a) |
| notes | varchar | 200 | yes | Modern_Spanish_CI_AS | no |
| pubdate | datetime | 8 | yes |  | (n/a) |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| DWH | title | I | 02/11/2017 15:57:17 | 02/11/2017 15:57:20 | S | DESKTOP-HCA06TJ\Pablo Corral | 18 | 0 | 0 |

#### dim.title_Changes {#head_dim_title_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| title$Changes | dim | dbo | 02/11/2017 15:56:30 | 18 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_title | int | 4 | yes |  | (n/a) |
| idtitle | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| title | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
| type | char | 12 | yes | Modern_Spanish_CI_AS | no |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| price | money | 8 | yes |  | (n/a) |
| advance | money | 8 | yes |  | (n/a) |
| royalty | int | 4 | yes |  | (n/a) |
| ytd_sales | int | 4 | yes |  | (n/a) |
| notes | varchar | 200 | yes | Modern_Spanish_CI_AS | no |
| pubdate | datetime | 8 | yes |  | (n/a) |
| fromdate | datetime | 8 | yes |  | (n/a) |
| todate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash_T1 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T2 | bigint | 8 | yes |  | (n/a) |
| $sq_row_hash_T1h | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### fact.sales {#head_fact_sales}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales | fact | dbo | 02/11/2017 15:56:40 | 23 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_sales | int | 4 | no |  | (n/a) |
| id_sk_author | int | 4 | yes |  | (n/a) |
| id_sk_publisher | int | 4 | yes |  | (n/a) |
| id_sk_store | int | 4 | yes |  | (n/a) |
| id_sk_title | int | 4 | yes |  | (n/a) |
| idsales | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| idstore | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| qty | smallint | 2 | yes |  | (n/a) |
| payterms | varchar | 12 | yes | Modern_Spanish_CI_AS | no |
| idtitle | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| idauthor | varchar | 11 | yes | Modern_Spanish_CI_AS | no |
| idpublisher | char | 4 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |
| version | tinyint | 1 | no |  | (n/a) |
| iddummyTiempo | tinyint | 1 | yes |  | (n/a) |
| idProcessDAte | int | 4 | no |  | (n/a) |
| contador | int | 4 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| DWH | sales | F | 02/11/2017 15:57:21 | 02/11/2017 15:57:23 | S | DESKTOP-HCA06TJ\Pablo Corral | 23 | 0 | 0 |
| stg | sales | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\Pablo Corral | 21 | 0 | 0 |

#### fact.sales_Changes {#head_fact_sales_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales$Changes | fact | dbo | 02/11/2017 15:56:40 | 23 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| sk_sales | int | 4 | yes |  | (n/a) |
| id_sk_author | int | 4 | yes |  | (n/a) |
| id_sk_publisher | int | 4 | yes |  | (n/a) |
| id_sk_store | int | 4 | yes |  | (n/a) |
| id_sk_title | int | 4 | yes |  | (n/a) |
| idsales | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| idstore | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| qty | smallint | 2 | yes |  | (n/a) |
| payterms | varchar | 12 | yes | Modern_Spanish_CI_AS | no |
| idtitle | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| idauthor | varchar | 11 | yes | Modern_Spanish_CI_AS | no |
| idpublisher | char | 4 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |


### Vistas

