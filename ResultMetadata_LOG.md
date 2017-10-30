![SolidQ Logo](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif "Logo Title Text 1")
# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tablas](#head_tablas)
  * [log.etl_table_load_info](#head_log.etl_table_load_info)
  * [log.test_etl_table_load_info](#head_log.test_etl_table_load_info)
  
* [Vistas](#head_vistas)
  * [log.Tables](#head_log.Tables)
  

## Info <a name="head_info"></a>
**ABA2017_LOG**

DB Info:

| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| ABA2017_LOG |     300.00 MB| sa| 11| Oct 26 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=852, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 130 |

Files:

| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| ABA_2017_LOG_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\ABA_2017_LOG_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| ABA_2017_LOG_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\ABA_2017_LOG_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| ABA_2017_LOG_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\ABA_2017_LOG_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tablas <a name="head_tablas"></a>

**log.etl_table_load_info** <a name="head_log.etl_table_load_info"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| etl_table_load_info | log | dbo | 26/10/2017 10:36:53 | 44 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| id | int | 4 | no |  | (n/a) |
| schema_name | sysname | 256 | no | Modern_Spanish_CI_AS | (n/a) |
| table_name | sysname | 256 | no | Modern_Spanish_CI_AS | (n/a) |
| type | char | 1 | no | Modern_Spanish_CI_AS | no |
| ssis_server_execution_id | bigint | 8 | no |  | (n/a) |
| start_date | datetime2 | 8 | no |  | (n/a) |
| end_date | datetime2 | 8 | yes |  | (n/a) |
| status | char | 1 | yes | Modern_Spanish_CI_AS | no |
| loaded_by | sysname | 256 | yes | Modern_Spanish_CI_AS | (n/a) |
| rows | bigint | 8 | yes |  | (n/a) |
| inserted_rows | int | 4 | yes |  | (n/a) |
| updated_rows | int | 4 | yes |  | (n/a) |
| deleted_rows | int | 4 | yes |  | (n/a) |
| UpdatedRowst1 | int | 4 | yes |  | (n/a) |
| UpdatedRowst1h | int | 4 | yes |  | (n/a) |
| UpdatedRowst2 | int | 4 | yes |  | (n/a) |
| $xcs | xml | -1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

**log.test_etl_table_load_info** <a name="head_log.test_etl_table_load_info"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| test_etl_table_load_info | log | dbo | 26/10/2017 10:36:53 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| id | int | 4 | no |  | (n/a) |
| test_name | nvarchar | 600 | no | Modern_Spanish_CI_AS | (n/a) |
| start_date | datetime2 | 8 | yes |  | (n/a) |
| end_date | datetime2 | 8 | yes |  | (n/a) |
| result | nvarchar | 100 | yes | Modern_Spanish_CI_AS | (n/a) |
| executed | nvarchar | 20 | yes | Modern_Spanish_CI_AS | (n/a) |
| message | nvarchar | 1000 | yes | Modern_Spanish_CI_AS | (n/a) |
| execution_id | int | 4 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |


### Vistas <a name="head_vistas"></a>

**log.Tables** <a name="head_log.Tables"></a>

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| Tables | log | dbo | 26/10/2017 10:36:53 | 15 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| TableType | varchar | 12 | no | Modern_Spanish_CI_AS | yes |
| table_name | sysname | 256 | no | Modern_Spanish_CI_AS | (n/a) |


Creation SQL Script:
```


create view [log].[Tables] As

select distinct 

    iif(table_name like 'Orquest%', 'Orchestrator', 'Tables') TableType

    ,table_name 

from [log].[etl_table_load_info]



```
</br>


