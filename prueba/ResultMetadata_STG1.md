![](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif)

# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tablas](#head_tables)
  * [stg.autores](#head_stg_autores)
  * [stg.autores$Changes](#head_stg_autores_Changes)
  * [stg.autores$Errors](#head_stg_autores_Errors)
  * [stg.writers](#head_stg_writers)
  * [stg.writers$Changes](#head_stg_writers_Changes)
  * [stg.writers$Errors](#head_stg_writers_Errors)
  * [stg.authors](#head_stg_authors)
  * [stg.authors$Changes](#head_stg_authors_Changes)
  * [stg.authors$Errors](#head_stg_authors_Errors)
  * [stg.publishers](#head_stg_publishers)
  * [stg.publishers$Changes](#head_stg_publishers_Changes)
  * [stg.publishers$Errors](#head_stg_publishers_Errors)
  * [stg.sales](#head_stg_sales)
  * [stg.sales$Changes](#head_stg_sales_Changes)
  * [stg.sales$Errors](#head_stg_sales_Errors)
  * [stg.stores](#head_stg_stores)
  * [stg.stores$Changes](#head_stg_stores_Changes)
  * [stg.stores$Errors](#head_stg_stores_Errors)
  * [stg.titleauthor](#head_stg_titleauthor)
  * [stg.titleauthor$Changes](#head_stg_titleauthor_Changes)
  * [stg.titleauthor$Errors](#head_stg_titleauthor_Errors)
  * [stg.titles](#head_stg_titles)
  * [stg.titles$Changes](#head_stg_titles_Changes)
  * [stg.titles$Errors](#head_stg_titles_Errors)
  
* [Vistas](#head_vistas)
  * [etl.vw_dim_title](#head_etl_vw_dim_title)
  * [etl.vw_dim_author](#head_etl_vw_dim_author)
  * [etl.vw_dim_publisher](#head_etl_vw_dim_publisher)
  * [etl.vw_dim_store](#head_etl_vw_dim_store)
  * [etl.vw_fact_sales](#head_etl_vw_fact_sales)
  

## Info {#head_info}
**ABA2017_STG**

DB Info:

| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| ABA2017_STG |     300.00 MB| sa| 8| Nov  2 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=869, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 140 |

Files:

| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| ABA2017_STG_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_STG_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| ABA2017_STG_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_STG_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| ABA2017_STG_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_STG_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tables

#### stg.autores {#head_stg_autores}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| autores | stg | dbo | 13/11/2017 8:24:23 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| au_id | nvarchar | 100 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_lname | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_fname | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| phone | nchar | 24 | yes | Modern_Spanish_CI_AS | (n/a) |
| address | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| city | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| state | nchar | 4 | yes | Modern_Spanish_CI_AS | (n/a) |
| zip | nchar | 10 | yes | Modern_Spanish_CI_AS | (n/a) |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_execution_id_inserted | bigint | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | autores | F | 09/11/2017 16:44:48 | 09/11/2017 16:44:48 | S | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 16:07:58 | 09/11/2017 16:07:58 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 16:05:18 | 09/11/2017 16:05:19 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 16:04:54 | 09/11/2017 16:04:54 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 16:04:26 | 09/11/2017 16:04:26 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 15:59:04 | 09/11/2017 15:59:04 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 15:58:05 | 09/11/2017 15:58:06 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 15:57:01 | 09/11/2017 15:57:01 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 15:56:28 | 09/11/2017 15:56:29 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 14:27:01 | 09/11/2017 14:27:01 | S | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |

#### stg.autores_Changes {#head_stg_autores_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| autores$Changes | stg | dbo | 13/11/2017 8:24:23 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| au_id | nvarchar | 100 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_lname | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_fname | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| phone | nchar | 24 | yes | Modern_Spanish_CI_AS | (n/a) |
| address | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| city | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| state | nchar | 4 | yes | Modern_Spanish_CI_AS | (n/a) |
| zip | nchar | 10 | yes | Modern_Spanish_CI_AS | (n/a) |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.autores_Errors {#head_stg_autores_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| autores$Errors | stg | dbo | 13/11/2017 8:24:23 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| au_id | nvarchar | 100 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_lname | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_fname | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| phone | nchar | 24 | yes | Modern_Spanish_CI_AS | (n/a) |
| address | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| city | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| state | nchar | 4 | yes | Modern_Spanish_CI_AS | (n/a) |
| zip | nchar | 10 | yes | Modern_Spanish_CI_AS | (n/a) |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.writers {#head_stg_writers}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| writers | stg | dbo | 13/11/2017 8:35:25 | 23 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| au_id | nvarchar | 100 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_lname | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_fname | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| phone | nchar | 24 | yes | Modern_Spanish_CI_AS | (n/a) |
| address | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| city | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| state | nchar | 4 | yes | Modern_Spanish_CI_AS | (n/a) |
| zip | nchar | 10 | yes | Modern_Spanish_CI_AS | (n/a) |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_execution_id_inserted | bigint | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | writers | F | 13/11/2017 9:21:28 | 13/11/2017 9:21:28 | S | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 9:20:32 | 13/11/2017 9:20:32 | S | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 9:19:02 | 13/11/2017 9:19:02 | S | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 9:18:03 | 13/11/2017 9:18:04 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 9:17:31 | 13/11/2017 9:17:31 | F | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 8:53:07 | 13/11/2017 8:53:08 | S | DESKTOP-HCA06TJ\Pablo Corral |  |  |  |

#### stg.writers_Changes {#head_stg_writers_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| writers$Changes | stg | dbo | 13/11/2017 8:35:25 | 5 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| au_id | nvarchar | 100 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_lname | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_fname | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| phone | nchar | 24 | yes | Modern_Spanish_CI_AS | (n/a) |
| address | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| city | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| state | nchar | 4 | yes | Modern_Spanish_CI_AS | (n/a) |
| zip | nchar | 10 | yes | Modern_Spanish_CI_AS | (n/a) |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.writers_Errors {#head_stg_writers_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| writers$Errors | stg | dbo | 13/11/2017 8:35:25 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| au_id | nvarchar | 100 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_lname | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_fname | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| phone | nchar | 24 | yes | Modern_Spanish_CI_AS | (n/a) |
| address | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| city | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| state | nchar | 4 | yes | Modern_Spanish_CI_AS | (n/a) |
| zip | nchar | 10 | yes | Modern_Spanish_CI_AS | (n/a) |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.authors {#head_stg_authors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| authors | stg | dbo | 02/11/2017 15:51:05 | 23 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_au_id | varchar | 11 | no | Modern_Spanish_CI_AS | no |
| au_lname | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| au_fname | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| phone | char | 12 | yes | Modern_Spanish_CI_AS | no |
| address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_execution_id_inserted | bigint | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |
| 1  | NBi.NUnit.Runtime.TestSuite.Source.Helper.PK .authors.HLP-1.STG-1  | 04/10/2017 9:19:01  | 01/01/0001 0:00:00  | Success |  |
| 1  | NBi.NUnit.Runtime.TestSuite.Source.Helper.ERR.authors.HLP-1.STG-1  | 04/10/2017 9:19:01  | 01/01/0001 0:00:00  | Success |  |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | authors | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\Pablo Corral | 23 | 0 | 0 |

#### stg.authors_Changes {#head_stg_authors_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| authors$Changes | stg | dbo | 02/11/2017 15:51:05 | 23 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_au_id | varchar | 11 | no | Modern_Spanish_CI_AS | no |
| au_lname | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| au_fname | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| phone | char | 12 | yes | Modern_Spanish_CI_AS | no |
| address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.authors_Errors {#head_stg_authors_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| authors$Errors | stg | dbo | 02/11/2017 15:51:05 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_au_id | varchar | 11 | no | Modern_Spanish_CI_AS | no |
| au_lname | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| au_fname | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| phone | char | 12 | yes | Modern_Spanish_CI_AS | no |
| address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.publishers {#head_stg_publishers}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publishers | stg | dbo | 02/11/2017 15:51:05 | 8 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_pub_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| pub_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_execution_id_inserted | bigint | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | publishers | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\Pablo Corral | 8 | 0 | 0 |

#### stg.publishers_Changes {#head_stg_publishers_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publishers$Changes | stg | dbo | 02/11/2017 15:51:05 | 8 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_pub_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| pub_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.publishers_Errors {#head_stg_publishers_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publishers$Errors | stg | dbo | 02/11/2017 15:51:05 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_pub_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| pub_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.sales {#head_stg_sales}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales | stg | dbo | 02/11/2017 15:51:05 | 21 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| stor_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| ord_date | datetime | 8 | yes |  | (n/a) |
| qty | smallint | 2 | yes |  | (n/a) |
| payterms | varchar | 12 | yes | Modern_Spanish_CI_AS | no |
| title_id | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_execution_id_inserted | bigint | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| DWH | sales | F | 02/11/2017 15:57:21 | 02/11/2017 15:57:23 | S | DESKTOP-HCA06TJ\Pablo Corral | 23 | 0 | 0 |
| stg | sales | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\Pablo Corral | 21 | 0 | 0 |

#### stg.sales_Changes {#head_stg_sales_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales$Changes | stg | dbo | 02/11/2017 15:51:05 | 21 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| stor_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| ord_date | datetime | 8 | yes |  | (n/a) |
| qty | smallint | 2 | yes |  | (n/a) |
| payterms | varchar | 12 | yes | Modern_Spanish_CI_AS | no |
| title_id | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.sales_Errors {#head_stg_sales_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales$Errors | stg | dbo | 02/11/2017 15:51:05 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| stor_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| ord_date | datetime | 8 | yes |  | (n/a) |
| qty | smallint | 2 | yes |  | (n/a) |
| payterms | varchar | 12 | yes | Modern_Spanish_CI_AS | no |
| title_id | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.stores {#head_stg_stores}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| stores | stg | dbo | 02/11/2017 15:51:05 | 6 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_stor_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| stor_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| stor_address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_execution_id_inserted | bigint | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | stores | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\Pablo Corral | 6 | 0 | 0 |

#### stg.stores_Changes {#head_stg_stores_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| stores$Changes | stg | dbo | 02/11/2017 15:51:05 | 6 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_stor_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| stor_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| stor_address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.stores_Errors {#head_stg_stores_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| stores$Errors | stg | dbo | 02/11/2017 15:51:05 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_stor_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| stor_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| stor_address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.titleauthor {#head_stg_titleauthor}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titleauthor | stg | dbo | 02/11/2017 15:51:05 | 18 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 17 | no | Modern_Spanish_CI_AS | no |
| au_id | varchar | 11 | yes | Modern_Spanish_CI_AS | no |
| title_id | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| au_ord | tinyint | 1 | yes |  | (n/a) |
| royaltyper | int | 4 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_execution_id_inserted | bigint | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | titleauthor | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\Pablo Corral | 18 | 0 | 0 |

#### stg.titleauthor_Changes {#head_stg_titleauthor_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titleauthor$Changes | stg | dbo | 02/11/2017 15:51:05 | 18 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 17 | no | Modern_Spanish_CI_AS | no |
| au_id | varchar | 11 | yes | Modern_Spanish_CI_AS | no |
| title_id | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| au_ord | tinyint | 1 | yes |  | (n/a) |
| royaltyper | int | 4 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.titleauthor_Errors {#head_stg_titleauthor_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titleauthor$Errors | stg | dbo | 02/11/2017 15:51:05 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 17 | no | Modern_Spanish_CI_AS | no |
| au_id | varchar | 11 | yes | Modern_Spanish_CI_AS | no |
| title_id | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| au_ord | tinyint | 1 | yes |  | (n/a) |
| royaltyper | int | 4 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.titles {#head_stg_titles}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titles | stg | dbo | 02/11/2017 15:51:05 | 18 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_title_id | varchar | 6 | no | Modern_Spanish_CI_AS | no |
| title | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
| type | char | 12 | yes | Modern_Spanish_CI_AS | no |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| price | money | 8 | yes |  | (n/a) |
| advance | money | 8 | yes |  | (n/a) |
| royalty | int | 4 | yes |  | (n/a) |
| ytd_sales | int | 4 | yes |  | (n/a) |
| notes | varchar | 200 | yes | Modern_Spanish_CI_AS | no |
| pubdate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_execution_id_inserted | bigint | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | titles | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\Pablo Corral | 18 | 0 | 0 |

#### stg.titles_Changes {#head_stg_titles_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titles$Changes | stg | dbo | 02/11/2017 15:51:05 | 18 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_title_id | varchar | 6 | no | Modern_Spanish_CI_AS | no |
| title | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
| type | char | 12 | yes | Modern_Spanish_CI_AS | no |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| price | money | 8 | yes |  | (n/a) |
| advance | money | 8 | yes |  | (n/a) |
| royalty | int | 4 | yes |  | (n/a) |
| ytd_sales | int | 4 | yes |  | (n/a) |
| notes | varchar | 200 | yes | Modern_Spanish_CI_AS | no |
| pubdate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.titles_Errors {#head_stg_titles_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titles$Errors | stg | dbo | 02/11/2017 15:51:05 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_title_id | varchar | 6 | no | Modern_Spanish_CI_AS | no |
| title | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
| type | char | 12 | yes | Modern_Spanish_CI_AS | no |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| price | money | 8 | yes |  | (n/a) |
| advance | money | 8 | yes |  | (n/a) |
| royalty | int | 4 | yes |  | (n/a) |
| ytd_sales | int | 4 | yes |  | (n/a) |
| notes | varchar | 200 | yes | Modern_Spanish_CI_AS | no |
| pubdate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |


### Vistas

#### etl.vw_dim_title {#head_etl_vw_dim_title}

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_title | etl | dbo | 02/11/2017 15:53:24 | 18 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| idtitle | varchar | 6 | no | Modern_Spanish_CI_AS | no |
| title | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
| type | char | 12 | yes | Modern_Spanish_CI_AS | no |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| price | money | 8 | yes |  | (n/a) |
| advance | money | 8 | yes |  | (n/a) |
| royalty | int | 4 | yes |  | (n/a) |
| ytd_sales | int | 4 | yes |  | (n/a) |
| notes | varchar | 200 | yes | Modern_Spanish_CI_AS | no |
| pubdate | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |


Creation SQL Script:
```


create view etl.vw_dim_title as

SELECT [pk_title_id] as idtitle

      ,[title]

      ,[type]

      ,[pub_id]

      ,[price]

      ,[advance]

      ,[royalty]

      ,[ytd_sales]

      ,[notes]

      ,[pubdate]

      ,[$sq_row_hash]

      ,[$sq_execution_id]

  FROM [stg].[titles]

```




#### etl.vw_dim_author {#head_etl_vw_dim_author}

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_author | etl | dbo | 02/11/2017 15:53:24 | 23 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| idauthor | varchar | 11 | no | Modern_Spanish_CI_AS | no |
| au_lname | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| au_fname | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| phone | char | 12 | yes | Modern_Spanish_CI_AS | no |
| address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| contract | bit | 1 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |


Creation SQL Script:
```


CREATE view etl.vw_dim_author as 

SELECT [pk_au_id] as idauthor

      ,[au_lname]

      ,[au_fname]

      ,[phone]

      ,[address]

      ,[city]

      ,[state]

      ,[zip]

      ,[contract]

      ,[$sq_row_hash]

      ,[$sq_execution_id]

  FROM [stg].[authors]

```




#### etl.vw_dim_publisher {#head_etl_vw_dim_publisher}

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_publisher | etl | dbo | 02/11/2017 15:53:24 | 8 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| idpublisher | char | 4 | no | Modern_Spanish_CI_AS | no |
| pub_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |


Creation SQL Script:
```


CREATE view etl.vw_dim_publisher as

SELECT [pk_pub_id] as idpublisher

      ,[pub_name]

      ,[city]

      ,[state]

      ,[country]

      ,[$sq_row_hash]

      ,[$sq_execution_id]

  FROM [stg].[publishers]

```




#### etl.vw_dim_store {#head_etl_vw_dim_store}

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_store | etl | dbo | 02/11/2017 15:53:24 | 6 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| idstore | char | 4 | no | Modern_Spanish_CI_AS | no |
| stor_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| stor_address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |


Creation SQL Script:
```


CREATE view etl.vw_dim_store as 

SELECT [pk_stor_id] as idstore

      ,[stor_name]

      ,[stor_address]

      ,[city]

      ,[state]

      ,[zip]

      ,[$sq_row_hash]

      ,[$sq_execution_id]

  FROM [stg].[stores]

```




#### etl.vw_fact_sales {#head_etl_vw_fact_sales}

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_fact_sales | etl | dbo | 02/11/2017 15:53:24 | 23 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| idsales | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| idstore | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| qty | smallint | 2 | yes |  | (n/a) |
| payterms | varchar | 12 | yes | Modern_Spanish_CI_AS | no |
| idtitle | varchar | 6 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| idauthor | varchar | 11 | yes | Modern_Spanish_CI_AS | no |
| idpublisher | char | 4 | yes | Modern_Spanish_CI_AS | no |
| $sq_execution_id | bigint | 8 | yes |  | (n/a) |


Creation SQL Script:
```








CREATE view etl.vw_fact_sales as

SELECT T1.[pk_id] as idsales

      ,[stor_id] as idstore 

      ,[ord_num]

      ,[qty]

      ,[payterms]

      ,T1.[title_id] as idtitle

      ,T1.[$sq_row_hash]

	  ,T2.au_id as idauthor

	  ,T3.pub_id as idpublisher

	  ,p.idmax as '$sq_execution_id'

  FROM [stg].[sales] T1

  Inner Join stg.titleauthor T2 On T1.title_id = T2.title_id

  Inner Join stg.titles T3 On T1.title_id = T3.pk_title_id

  cross apply (select max(iddest) from ( select T1.[$sq_execution_id] as iddest union all select T2.[$sq_execution_id] union all select T3.[$sq_execution_id]) 

  a) as p(idmax) 



```




