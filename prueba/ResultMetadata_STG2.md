![](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif)

# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tablas](#head_tables)
  * [stg.newspapers](#head_stg_newspapers)
  * [stg.newspapers$Changes](#head_stg_newspapers_Changes)
  * [stg.newspapers$Errors](#head_stg_newspapers_Errors)
  * [stg.employee](#head_stg_employee)
  * [stg.employee$Changes](#head_stg_employee_Changes)
  * [stg.employee$Errors](#head_stg_employee_Errors)
  
* [Vistas](#head_vistas)
  * [etl.vw_dim_newspapers](#head_etl_vw_dim_newspapers)
  

## Info {#head_info}
**ABA2017_STG2**

DB Info:

| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| ABA2017_STG2 |     300.00 MB| DESKTOP-HCA06TJ\Pablo Corral| 13| Nov  2 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=869, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 130 |

Files:

| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| ABA2017_STG2_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_STG2_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| ABA2017_STG2_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_STG2_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| ABA2017_STG2_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_STG2_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tables

#### stg.newspapers {#head_stg_newspapers}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers | stg | dbo | 02/11/2017 15:51:05 | 6 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_np_id | int | 4 | no |  | (n/a) |
| name | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
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
| DWH | newspapers | I | 02/11/2017 15:57:08 | 02/11/2017 15:57:09 | S | DESKTOP-HCA06TJ\Pablo Corral | 6 | 0 | 0 |
| stg | newspapers | I | 02/11/2017 15:51:51 | 02/11/2017 15:51:52 | S | DESKTOP-HCA06TJ\Pablo Corral | 6 | 0 | 0 |

#### stg.newspapers_Changes {#head_stg_newspapers_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers$Changes | stg | dbo | 02/11/2017 15:51:05 | 6 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_np_id | int | 4 | no |  | (n/a) |
| name | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
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

#### stg.newspapers_Errors {#head_stg_newspapers_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers$Errors | stg | dbo | 02/11/2017 15:51:05 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_np_id | int | 4 | no |  | (n/a) |
| name | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
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

#### stg.employee {#head_stg_employee}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| employee | stg | dbo | 16/11/2017 16:05:00 | 42 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| emp_id | varchar | 50 | no | Modern_Spanish_CI_AS | no |
| fname | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| minit | char | 1 | yes | Modern_Spanish_CI_AS | no |
| lname | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| job_id | smallint | 2 | yes |  | (n/a) |
| job_lvl | tinyint | 1 | yes |  | (n/a) |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| hire_date | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_execution_id_inserted | bigint | 8 | no |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | employee | I | 16/11/2017 16:14:47 | 16/11/2017 16:14:48 | S | DESKTOP-HCA06TJ\Pablo Corral | 0 | 0 | 1 |
| stg | employee | I | 16/11/2017 16:05:11 | 16/11/2017 16:05:12 | S | DESKTOP-HCA06TJ\Pablo Corral | 43 | 0 | 0 |

#### stg.employee_Changes {#head_stg_employee_Changes}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| employee$Changes | stg | dbo | 16/11/2017 16:05:00 | 1 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| emp_id | varchar | 50 | no | Modern_Spanish_CI_AS | no |
| fname | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| minit | char | 1 | yes | Modern_Spanish_CI_AS | no |
| lname | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| job_id | smallint | 2 | yes |  | (n/a) |
| job_lvl | tinyint | 1 | yes |  | (n/a) |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| hire_date | datetime | 8 | yes |  | (n/a) |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |
| $sq_operation_id | tinyint | 1 | yes |  | (n/a) |


Unit tests:

| Execution id | Test name | Start date | End date | Result | Message |
| ------------ | --------- | ---------- | -------- | ------ | ------- |

Logs:

| Schema Name | Table Name | Type | Start Date | End Date | Status | Loaded by | Inserted Rows | Updated Rows | Deleted Rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |

#### stg.employee_Errors {#head_stg_employee_Errors}

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| employee$Errors | stg | dbo | 16/11/2017 16:05:00 | 0 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| emp_id | varchar | 50 | no | Modern_Spanish_CI_AS | no |
| fname | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| minit | char | 1 | yes | Modern_Spanish_CI_AS | no |
| lname | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| job_id | smallint | 2 | yes |  | (n/a) |
| job_lvl | tinyint | 1 | yes |  | (n/a) |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| hire_date | datetime | 8 | yes |  | (n/a) |
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

#### etl.vw_dim_newspapers {#head_etl_vw_dim_newspapers}

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_newspapers | etl | dbo | 02/11/2017 15:53:24 | 6 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| idnewspapers | int | 4 | no |  | (n/a) |
| name | varchar | 80 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |
| $sq_row_hash | bigint | 8 | yes |  | (n/a) |
| $sq_execution_id | bigint | 8 | no |  | (n/a) |


Creation SQL Script:
```
create view etl.vw_dim_newspapers as

SELECT 

	[pk_np_id] as idnewspapers,

	[name],

	[country],

	[$sq_row_hash],

	[$sq_execution_id]

  FROM [stg].[newspapers]

```



