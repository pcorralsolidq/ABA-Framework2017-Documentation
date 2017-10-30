![SolidQ Logo](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif "Logo Title Text 1")
# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tablas](#head_tablas)
  * [stg.authors](#head_stg.authors)
  * [stg.authors$Changes](#head_stg.authors$Changes)
  * [err.authors](#head_err.authors)
  * [stg.publishers](#head_stg.publishers)
  * [stg.publishers$Changes](#head_stg.publishers$Changes)
  * [err.publishers](#head_err.publishers)
  * [stg.sales](#head_stg.sales)
  * [stg.sales$Changes](#head_stg.sales$Changes)
  * [err.sales](#head_err.sales)
  * [stg.stores](#head_stg.stores)
  * [stg.stores$Changes](#head_stg.stores$Changes)
  * [err.stores](#head_err.stores)
  * [stg.titleauthor](#head_stg.titleauthor)
  * [stg.titleauthor$Changes](#head_stg.titleauthor$Changes)
  * [err.titleauthor](#head_err.titleauthor)
  * [stg.titles](#head_stg.titles)
  * [stg.titles$Changes](#head_stg.titles$Changes)
  * [err.titles](#head_err.titles)
  
* [Vistas](#head_vistas)
  * [etl.vw_dim_title](#head_etl.vw_dim_title)
  * [etl.vw_dim_author](#head_etl.vw_dim_author)
  * [etl.vw_dim_publisher](#head_etl.vw_dim_publisher)
  * [etl.vw_dim_store](#head_etl.vw_dim_store)
  * [etl.vw_fact_sales](#head_etl.vw_fact_sales)
  

## Info <a name="head_info"></a>
**Abamulti_STG**

DB Info:
| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| Abamulti_STG |     300.00 MB| sa| 8| Oct  8 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=852, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 130 |

Files:
| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| Abamulti_STG_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\Abamulti_STG_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| Abamulti_STG_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\Abamulti_STG_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| Abamulti_STG_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\Abamulti_STG_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tablas <a name="head_tablas"></a>

**stg.authors** <a name="head_stg.authors"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| authors | stg | dbo | 08/10/2017 20:44:37 | 23 |

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
| stg | authors | I | 09/10/2017 9:05:02 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 23 | 0 | 0 |

**stg.authors$Changes** <a name="head_stg.authors$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| authors$Changes | stg | dbo | 08/10/2017 20:44:37 | 23 |

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

**err.authors** <a name="head_err.authors"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| authors | err | dbo | 08/10/2017 20:44:37 | 0 |

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
| 1  | NBi.NUnit.Runtime.TestSuite.Source.Helper.PK .authors.HLP-1.STG-1  | 04/10/2017 9:19:01  | 01/01/0001 0:00:00  | Success |  |
| 1  | NBi.NUnit.Runtime.TestSuite.Source.Helper.ERR.authors.HLP-1.STG-1  | 04/10/2017 9:19:01  | 01/01/0001 0:00:00  | Success |  |

Logs:
| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | authors | I | 09/10/2017 9:05:02 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 23 | 0 | 0 |

**stg.publishers** <a name="head_stg.publishers"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publishers | stg | dbo | 08/10/2017 20:44:37 | 8 |

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
| stg | publishers | I | 09/10/2017 9:05:02 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 8 | 0 | 0 |

**stg.publishers$Changes** <a name="head_stg.publishers$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publishers$Changes | stg | dbo | 08/10/2017 20:44:37 | 8 |

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

**err.publishers** <a name="head_err.publishers"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publishers | err | dbo | 08/10/2017 20:44:37 | 0 |

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
| stg | publishers | I | 09/10/2017 9:05:02 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 8 | 0 | 0 |

**stg.sales** <a name="head_stg.sales"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales | stg | dbo | 08/10/2017 20:44:37 | 21 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| stor_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| incremental | bigint | 8 | yes |  | (n/a) |
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
| stg | sales | I | 09/10/2017 9:05:03 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 21 | 0 | 0 |

**stg.sales$Changes** <a name="head_stg.sales$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales$Changes | stg | dbo | 08/10/2017 20:44:37 | 21 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| stor_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| incremental | bigint | 8 | yes |  | (n/a) |
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

**err.sales** <a name="head_err.sales"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales | err | dbo | 08/10/2017 20:44:37 | 0 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| stor_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| incremental | bigint | 8 | yes |  | (n/a) |
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
| stg | sales | I | 09/10/2017 9:05:03 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 21 | 0 | 0 |

**stg.stores** <a name="head_stg.stores"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| stores | stg | dbo | 08/10/2017 20:44:37 | 6 |

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
| stg | stores | I | 09/10/2017 9:05:02 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |

**stg.stores$Changes** <a name="head_stg.stores$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| stores$Changes | stg | dbo | 08/10/2017 20:44:37 | 6 |

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

**err.stores** <a name="head_err.stores"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| stores | err | dbo | 08/10/2017 20:44:37 | 0 |

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
| stg | stores | I | 09/10/2017 9:05:02 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |

**stg.titleauthor** <a name="head_stg.titleauthor"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titleauthor | stg | dbo | 08/10/2017 20:44:37 | 18 |

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
| stg | titleauthor | I | 09/10/2017 9:05:02 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 18 | 0 | 0 |

**stg.titleauthor$Changes** <a name="head_stg.titleauthor$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titleauthor$Changes | stg | dbo | 08/10/2017 20:44:37 | 18 |

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

**err.titleauthor** <a name="head_err.titleauthor"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titleauthor | err | dbo | 08/10/2017 20:44:37 | 0 |

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
| stg | titleauthor | I | 09/10/2017 9:05:02 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 18 | 0 | 0 |

**stg.titles** <a name="head_stg.titles"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titles | stg | dbo | 08/10/2017 20:44:37 | 18 |

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
| stg | titles | I | 09/10/2017 9:05:03 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 18 | 0 | 0 |

**stg.titles$Changes** <a name="head_stg.titles$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titles$Changes | stg | dbo | 08/10/2017 20:44:37 | 18 |

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

**err.titles** <a name="head_err.titles"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| titles | err | dbo | 08/10/2017 20:44:37 | 0 |

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
| stg | titles | I | 09/10/2017 9:05:03 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 18 | 0 | 0 |


### Vistas <a name="head_vistas"></a>

**etl.vw_dim_title** <a name="head_etl.vw_dim_title"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_title | etl | dbo | 09/10/2017 9:29:51 | 18 |

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
</br>


**etl.vw_dim_author** <a name="head_etl.vw_dim_author"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_author | etl | dbo | 09/10/2017 9:29:51 | 23 |

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
</br>


**etl.vw_dim_publisher** <a name="head_etl.vw_dim_publisher"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_publisher | etl | dbo | 09/10/2017 9:29:51 | 8 |

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
</br>


**etl.vw_dim_store** <a name="head_etl.vw_dim_store"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_store | etl | dbo | 09/10/2017 9:29:51 | 6 |

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
</br>


**etl.vw_fact_sales** <a name="head_etl.vw_fact_sales"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_fact_sales | etl | dbo | 09/10/2017 9:29:51 | 23 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| idsales | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| idstore | char | 4 | yes | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| incremental | bigint | 8 | yes |  | (n/a) |
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

      ,[incremental]

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
</br>


