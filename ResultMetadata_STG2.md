![SolidQ Logo](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif "Logo Title Text 1")
# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tablas](#head_tablas)
  * [stg.newspapers](#head_stg.newspapers)
  * [stg.newspapers$Changes](#head_stg.newspapers$Changes)
  * [stg.newspapers$Errors](#head_stg.newspapers$Errors)
  
* [Vistas](#head_vistas)
  * [etl.vw_dim_newspapers](#head_etl.vw_dim_newspapers)
  

## Info <a name="head_info"></a>
**ABA_2017_STG2**

DB Info:

| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| ABA_2017_STG2 |     300.00 MB| DESKTOP-F9SD47Q\pcl23| 13| Oct 26 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=852, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 130 |

Files:

| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| ABA_2017_STG2_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\ABA_2017_STG2_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| ABA_2017_STG2_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\ABA_2017_STG2_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| ABA_2017_STG2_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\ABA_2017_STG2_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tablas <a name="head_tablas"></a>

**stg.newspapers** <a name="head_stg.newspapers"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers | stg | dbo | 26/10/2017 11:29:10 | 6 |

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
| DWH | newspapers | I | 26/10/2017 16:54:46 | 26/10/2017 16:54:47 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| DWH | newspapers | I | 26/10/2017 16:52:14 | 26/10/2017 16:52:15 | S | MicrosoftAccount\pcl23ua@gmail.com | 0 | 0 | 0 |
| DWH | newspapers | I | 26/10/2017 16:45:11 | 26/10/2017 16:45:12 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| stg | newspapers | I | 26/10/2017 13:56:07 | 26/10/2017 13:56:08 | F | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| DWH | newspapers | I | 26/10/2017 13:25:11 | 26/10/2017 13:25:12 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 | 0 |
| stg | newspapers | F | 26/10/2017 12:55:35 | 26/10/2017 12:55:35 | S | MicrosoftAccount\pcl23ua@gmail.com | 6 | 0 |  |

**stg.newspapers$Changes** <a name="head_stg.newspapers$Changes"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers$Changes | stg | dbo | 26/10/2017 11:29:10 | 6 |

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

**stg.newspapers$Errors** <a name="head_stg.newspapers$Errors"></a>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| newspapers$Errors | stg | dbo | 26/10/2017 11:29:10 | 0 |

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


### Vistas <a name="head_vistas"></a>

**etl.vw_dim_newspapers** <a name="head_etl.vw_dim_newspapers"></a>

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| vw_dim_newspapers | etl | dbo | 26/10/2017 13:04:57 | 6 |

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
</br>


