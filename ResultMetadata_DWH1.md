![SolidQ Logo](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif "Logo Title Text 1")
# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tablas](#head_tablas)
  * [dim.store$Changes](#head_dim.store$Changes)
  * [dim.title](#head_dim.title)
  * [dim.title$Changes](#head_dim.title$Changes)
  * [fact.sales](#head_fact.sales)
  * [fact.sales$Changes](#head_fact.sales$Changes)
  * [dim.author](#head_dim.author)
  * [dim.author$Changes](#head_dim.author$Changes)
  * [dim.newspapers](#head_dim.newspapers)
  * [dim.newspapers$Changes](#head_dim.newspapers$Changes)
  * [dim.publisher](#head_dim.publisher)
  * [dim.publisher$Changes](#head_dim.publisher$Changes)
  * [dim.store](#head_dim.store)
  
* [Vistas](#head_vistas)
  

## Info <a name="head_info"></a>
**ABA_2017_DWH**

DB Info:

| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| ABA_2017_DWH |     300.00 MB| sa| 7| Oct 26 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=852, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 130 |

Files:

| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| ABA_2017_DWH_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\ABA_2017_DWH_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| ABA_2017_DWH_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\ABA_2017_DWH_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| ABA_2017_DWH_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\ABA_2017_DWH_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tablas <a name="head_tablas"></a>

**dim.store$Changes** <a name="head_dim.store$Changes"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| store$Changes | dim | dbo | 26/10/2017 16:54:02 | 6 |

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

**dim.title** <a name="head_dim.title"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| title | dim | dbo | 26/10/2017 16:54:02 | 19 |

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
| DWH | title | I | 26/10/2017 16:54:54 | 26/10/2017 16:54:58 | S | MicrosoftAccount\pcl23ua@gmail.com | 18 | 0 | 0 |
| DWH | title | I | 26/10/2017 16:52:22 | 26/10/2017 16:52:25 | S | MicrosoftAccount\pcl23ua@gmail.com | 18 | 0 | 0 |
| DWH | title | I | 26/10/2017 13:25:56 | 26/10/2017 13:25:59 | S | MicrosoftAccount\pcl23ua@gmail.com | 18 | 0 | 0 |

**dim.title$Changes** <a name="head_dim.title$Changes"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| title$Changes | dim | dbo | 26/10/2017 16:54:02 | 18 |

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

**fact.sales** <a name="head_fact.sales"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales | fact | dbo | 26/10/2017 16:52:00 | 23 |

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
| DWH | sales | F | 26/10/2017 16:54:58 | 26/10/2017 16:54:59 | S | MicrosoftAccount\pcl23ua@gmail.com | 0 | 0 | 0 |
| DWH | sales | F | 26/10/2017 16:52:26 | 26/10/2017 16:52:27 | S | MicrosoftAccount\pcl23ua@gmail.com | 23 | 0 | 0 |
| stg | sales | F | 26/10/2017 12:43:48 | 26/10/2017 12:43:52 | S | MicrosoftAccount\pcl23ua@gmail.com | 21 | 0 |  |

**fact.sales$Changes** <a name="head_fact.sales$Changes"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales$Changes | fact | dbo | 26/10/2017 16:52:00 | 0 |

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

**dim.author** <a name="head_dim.author"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| author | dim | dbo | 26/10/2017 16:54:02 | 24 |

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
| DWH | author | I | 26/10/2017 16:54:54 | 26/10/2017 16:54:58 | S | MicrosoftAccount\pcl23ua@gmail.com | 23 | 0 | 0 |
| DWH | author | I | 26/10/2017 16:52:22 | 26/10/2017 16:52:25 | S | MicrosoftAccount\pcl23ua@gmail.com | 23 | 0 | 0 |
| DWH | author | I | 26/10/2017 13:25:56 | 26/10/2017 13:25:59 | S | MicrosoftAccount\pcl23ua@gmail.com | 23 | 0 | 0 |

**dim.author$Changes** <a name="head_dim.author$Changes"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| author$Changes | dim | dbo | 26/10/2017 16:54:02 | 23 |

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

**dim.newspapers** <a name="head_dim.newspapers"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers | dim | dbo | 26/10/2017 16:54:02 | 7 |

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
| DWH | newspapers | I | 26/10/2017 16:54:46 | 26/10/2017 16:54:47 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| DWH | newspapers | I | 26/10/2017 16:52:14 | 26/10/2017 16:52:15 | S | MicrosoftAccount\pcl23ua@gmail.com | 0 | 0 | 0 |
| DWH | newspapers | I | 26/10/2017 16:45:11 | 26/10/2017 16:45:12 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| stg | newspapers | I | 26/10/2017 13:56:07 | 26/10/2017 13:56:08 | F | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| DWH | newspapers | I | 26/10/2017 13:25:11 | 26/10/2017 13:25:12 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| stg | newspapers | F | 26/10/2017 12:55:35 | 26/10/2017 12:55:35 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 |  |

**dim.newspapers$Changes** <a name="head_dim.newspapers$Changes"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers$Changes | dim | dbo | 26/10/2017 16:54:02 | 6 |

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

**dim.publisher** <a name="head_dim.publisher"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publisher | dim | dbo | 26/10/2017 16:54:02 | 9 |

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
| DWH | publisher | I | 26/10/2017 16:54:54 | 26/10/2017 16:54:58 | S | MicrosoftAccount\pcl23ua@gmail.com | 8 | 0 | 0 |
| DWH | publisher | I | 26/10/2017 16:52:21 | 26/10/2017 16:52:25 | S | MicrosoftAccount\pcl23ua@gmail.com | 8 | 0 | 0 |
| DWH | publisher | I | 26/10/2017 13:25:56 | 26/10/2017 13:25:59 | S | MicrosoftAccount\pcl23ua@gmail.com | 8 | 0 | 0 |

**dim.publisher$Changes** <a name="head_dim.publisher$Changes"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publisher$Changes | dim | dbo | 26/10/2017 16:54:02 | 8 |

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

**dim.store** <a name="head_dim.store"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| store | dim | dbo | 26/10/2017 16:54:02 | 7 |

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
| DWH | store | I | 26/10/2017 16:54:54 | 26/10/2017 16:54:58 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| DWH | store | I | 26/10/2017 16:52:22 | 26/10/2017 16:52:25 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| DWH | store | I | 26/10/2017 13:25:56 | 26/10/2017 13:25:59 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |


### Vistas <a name="head_vistas"></a>

