![](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif)

# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tables](#head_tables)
  * [dbo.systranschemas](#dbo.systranschemas)
  * [cdc.change_tables](#cdc.change_tables)
  * [cdc.ddl_history](#cdc.ddl_history)
  * [cdc.lsn_time_mapping](#cdc.lsn_time_mapping)
  * [cdc.captured_columns](#cdc.captured_columns)
  * [cdc.index_columns](#cdc.index_columns)
  * [dbo.writers](#dbo.writers)
  * [cdc.dbo_writers_CT](#cdc.dbo_writers_CT)
  * [dbo.cdc_states](#dbo.cdc_states)
  * [dbo.employee](#dbo.employee)
  
* [Views](#head_views)
  

## Info <a name='head_info'>
**CDC_Demo**

DB Info:

| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| CDC_Demo |      80.00 MB| DESKTOP-HCA06TJ\Pablo Corral| 14| Nov  9 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=FULL, Version=869, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 140 |

Files:

| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| CDC_Demo | 1 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\CDC_Demo.mdf | PRIMARY | 8192 KB | Unlimited | 65536 KB |
| CDC_Demo_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\CDC_Demo_log.ldf |  | 73728 KB | 2147483648 KB | 65536 KB |

### Tables <a name='head_tables'>

#### dbo.systranschemas <a name='dbo.systranschemas'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| systranschemas | dbo | dbo | 09/11/2017 17:43:50 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| tabid | int | 4 | no |  | (n/a) |
| startlsn | binary | 10 | no |  | no |
| endlsn | binary | 10 | no |  | no |
| typeid | int | 4 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### cdc.change_tables <a name='cdc.change_tables'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| change_tables | cdc | cdc | 09/11/2017 17:43:50 | 1 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| object_id | int | 4 | no |  | (n/a) |
| version | int | 4 | yes |  | (n/a) |
| source_object_id | int | 4 | yes |  | (n/a) |
| capture_instance | sysname | 256 | no | Modern_Spanish_CI_AS | (n/a) |
| start_lsn | binary | 10 | yes |  | no |
| end_lsn | binary | 10 | yes |  | no |
| supports_net_changes | bit | 1 | yes |  | (n/a) |
| has_drop_pending | bit | 1 | yes |  | (n/a) |
| role_name | sysname | 256 | yes | Modern_Spanish_CI_AS | (n/a) |
| index_name | sysname | 256 | yes | Modern_Spanish_CI_AS | (n/a) |
| filegroup_name | sysname | 256 | yes | Modern_Spanish_CI_AS | (n/a) |
| create_date | datetime | 8 | yes |  | (n/a) |
| partition_switch | bit | 1 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### cdc.ddl_history <a name='cdc.ddl_history'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| ddl_history | cdc | cdc | 09/11/2017 17:43:50 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| source_object_id | int | 4 | yes |  | (n/a) |
| object_id | int | 4 | no |  | (n/a) |
| required_column_update | bit | 1 | yes |  | (n/a) |
| ddl_command | nvarchar | -1 | yes | Modern_Spanish_CI_AS | (n/a) |
| ddl_lsn | binary | 10 | no |  | no |
| ddl_time | datetime | 8 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### cdc.lsn_time_mapping <a name='cdc.lsn_time_mapping'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| lsn_time_mapping | cdc | cdc | 09/11/2017 17:43:50 | 235 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| start_lsn | binary | 10 | no |  | no |
| tran_begin_time | datetime | 8 | yes |  | (n/a) |
| tran_end_time | datetime | 8 | yes |  | (n/a) |
| tran_id | varbinary | 10 | yes |  | no |
| tran_begin_lsn | binary | 10 | yes |  | no |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### cdc.captured_columns <a name='cdc.captured_columns'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| captured_columns | cdc | cdc | 09/11/2017 17:43:50 | 9 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| object_id | int | 4 | no |  | (n/a) |
| column_name | sysname | 256 | no | Modern_Spanish_CI_AS | (n/a) |
| column_id | int | 4 | yes |  | (n/a) |
| column_type | sysname | 256 | no | Modern_Spanish_CI_AS | (n/a) |
| column_ordinal | int | 4 | no |  | (n/a) |
| is_computed | bit | 1 | yes |  | (n/a) |
| masking_function | nvarchar | 8000 | yes | Latin1_General_CI_AS_KS_WS | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### cdc.index_columns <a name='cdc.index_columns'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| index_columns | cdc | cdc | 09/11/2017 17:43:50 | 1 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| object_id | int | 4 | no |  | (n/a) |
| column_name | sysname | 256 | no | Modern_Spanish_CI_AS | (n/a) |
| index_ordinal | tinyint | 1 | no |  | (n/a) |
| column_id | int | 4 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### dbo.writers <a name='dbo.writers'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| writers | dbo | dbo | 09/11/2017 18:00:05 | 23 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| au_id | nvarchar | 100 | no | Modern_Spanish_CI_AS | (n/a) |
| au_lname | nvarchar | 80 | no | Modern_Spanish_CI_AS | (n/a) |
| au_fname | nvarchar | 40 | no | Modern_Spanish_CI_AS | (n/a) |
| phone | nchar | 24 | no | Modern_Spanish_CI_AS | (n/a) |
| address | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| city | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| state | nchar | 4 | yes | Modern_Spanish_CI_AS | (n/a) |
| zip | nchar | 10 | yes | Modern_Spanish_CI_AS | (n/a) |
| contract | bit | 1 | no |  | (n/a) |


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

#### cdc.dbo_writers_CT <a name='cdc.dbo_writers_CT'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| dbo_writers_CT | cdc | cdc | 09/11/2017 18:07:09 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| __$start_lsn | binary | 10 | no |  | no |
| __$end_lsn | binary | 10 | yes |  | no |
| __$seqval | binary | 10 | no |  | no |
| __$operation | int | 4 | no |  | (n/a) |
| __$update_mask | varbinary | 128 | yes |  | no |
| au_id | nvarchar | 100 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_lname | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| au_fname | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| phone | nchar | 24 | yes | Modern_Spanish_CI_AS | (n/a) |
| address | nvarchar | 80 | yes | Modern_Spanish_CI_AS | (n/a) |
| city | nvarchar | 40 | yes | Modern_Spanish_CI_AS | (n/a) |
| state | nchar | 4 | yes | Modern_Spanish_CI_AS | (n/a) |
| zip | nchar | 10 | yes | Modern_Spanish_CI_AS | (n/a) |
| contract | bit | 1 | yes |  | (n/a) |
| __$command_id | int | 4 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### dbo.cdc_states <a name='dbo.cdc_states'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| cdc_states | dbo | dbo | 13/11/2017 8:47:15 | 1 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| name | nvarchar | 512 | no | Modern_Spanish_CI_AS | (n/a) |
| state | nvarchar | 512 | no | Modern_Spanish_CI_AS | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### dbo.employee <a name='dbo.employee'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| employee | dbo | dbo | 16/11/2017 15:32:42 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| emp_id | varchar | 50 | no | Modern_Spanish_CI_AS | no |
| fname | varchar | 1 | no | Modern_Spanish_CI_AS | no |
| minit | char | 1 | yes | Modern_Spanish_CI_AS | no |
| lname | varchar | 1 | no | Modern_Spanish_CI_AS | no |
| job_id | smallint | 2 | no |  | (n/a) |
| job_lvl | tinyint | 1 | yes |  | (n/a) |
| pub_id | char | 1 | no | Modern_Spanish_CI_AS | no |
| hire_date | datetime | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | employee | I | 16/11/2017 16:14:47 | 16/11/2017 16:14:48 | S | DESKTOP-HCA06TJ\Pablo Corral | 0 | 0 | 1 |
| stg | employee | I | 16/11/2017 16:05:11 | 16/11/2017 16:05:12 | S | DESKTOP-HCA06TJ\Pablo Corral | 43 | 0 | 0 |


### Views <a name='head_views'>

