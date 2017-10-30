![SolidQ Logo](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif "Logo Title Text 1")
# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tablas](#head_tablas)
  * [fact.sales](#head_fact.sales)
  * [fact.sales$Changes](#head_fact.sales$Changes)
  * [dim.author](#head_dim.author)
  * [dim.author$Changes](#head_dim.author$Changes)
  * [dim.publisher](#head_dim.publisher)
  * [dim.publisher$Changes](#head_dim.publisher$Changes)
  * [dim.store](#head_dim.store)
  * [dim.store$Changes](#head_dim.store$Changes)
  * [dim.title](#head_dim.title)
  * [dim.title$Changes](#head_dim.title$Changes)
  
* [Vistas](#head_vistas)
  

## Info <a name="head_info"></a>
**Abamulti_DWH**

DB Info:
| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| Abamulti_DWH |     300.00 MB| sa| 7| Oct  8 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=852, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 130 |

Files:
| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| Abamulti_DWH_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\Abamulti_DWH_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| Abamulti_DWH_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\Abamulti_DWH_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| Abamulti_DWH_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\Abamulti_DWH_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tablas <a name="head_tablas"></a>

**fact.sales** <a name="head_fact.sales"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales | fact | dbo | 09/10/2017 10:25:07 | 0 |

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
| incremental | bigint | 8 | yes |  | (n/a) |
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
| stg | sales | I | 09/10/2017 9:05:03 | 09/10/2017 9:05:14 | S | MicrosoftAccount\pcl23ua@gmail.com | 21 | 0 | 0 |

**fact.sales$Changes** <a name="head_fact.sales$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| sales$Changes | fact | dbo | 09/10/2017 10:25:07 | 0 |

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
| incremental | bigint | 8 | yes |  | (n/a) |
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
| author | dim | dbo | 09/10/2017 10:25:58 | 24 |

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
| DWH | author | I | 09/10/2017 10:36:31 | 09/10/2017 10:36:36 | S | MicrosoftAccount\pcl23ua@gmail.com | 23 | 0 | 0 |

**dim.author$Changes** <a name="head_dim.author$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| author$Changes | dim | dbo | 09/10/2017 10:25:58 | 23 |

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

**dim.publisher** <a name="head_dim.publisher"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publisher | dim | dbo | 09/10/2017 10:25:59 | 9 |

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
| DWH | publisher | I | 09/10/2017 12:54:27 | 09/10/2017 12:54:28 | S | MicrosoftAccount\pcl23ua@gmail.com | 0 | 0 | 0 |
| DWH | publisher | I | 09/10/2017 10:36:31 | 09/10/2017 10:36:36 | S | MicrosoftAccount\pcl23ua@gmail.com | 8 | 0 | 0 |

**dim.publisher$Changes** <a name="head_dim.publisher$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| publisher$Changes | dim | dbo | 09/10/2017 10:25:59 | 0 |

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
| store | dim | dbo | 09/10/2017 10:25:59 | 7 |

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
| DWH | store | I | 09/10/2017 10:36:31 | 09/10/2017 10:36:36 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |

**dim.store$Changes** <a name="head_dim.store$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| store$Changes | dim | dbo | 09/10/2017 10:25:59 | 6 |

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
| title | dim | dbo | 09/10/2017 10:25:59 | 19 |

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
| DWH | title | I | 09/10/2017 10:36:31 | 09/10/2017 10:36:36 | S | MicrosoftAccount\pcl23ua@gmail.com | 18 | 0 | 0 |

**dim.title$Changes** <a name="head_dim.title$Changes"></a>

Table info:
| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| title$Changes | dim | dbo | 09/10/2017 10:25:59 | 18 |

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


### Vistas <a name="head_vistas"></a>

