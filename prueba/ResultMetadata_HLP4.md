![](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif)

# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tables](#head_tables)
  * [dbo.employee](#dbo.employee)
  
* [Views](#head_views)
  

## Info <a name='head_info'>
**CTC_Demo**

DB Info:

| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| CTC_Demo |      16.00 MB| DESKTOP-HCA06TJ\Pablo Corral| 15| Nov 16 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=FULL, Version=869, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 140 |

Files:

| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| CTC_DEMO | 1 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\CTC_DEMO.mdf | PRIMARY | 8192 KB | Unlimited | 65536 KB |
| CTC_DEMO_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\CTC_DEMO_log.ldf |  | 8192 KB | 2147483648 KB | 65536 KB |

### Tables <a name='head_tables'>

#### dbo.employee <a name='dbo.employee'>

Table info:

| Table name | Schema | Owner | Creation date | Rows |
| ---------- | ------ | ----- | ------------- | ---- |
| employee | dbo | dbo | 16/11/2017 15:41:40 | 42 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| emp_id | varchar | 50 | no | Modern_Spanish_CI_AS | no |
| fname | varchar | 20 | no | Modern_Spanish_CI_AS | no |
| minit | char | 1 | yes | Modern_Spanish_CI_AS | no |
| lname | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| job_id | smallint | 2 | no |  | (n/a) |
| job_lvl | tinyint | 1 | yes |  | (n/a) |
| pub_id | char | 4 | no | Modern_Spanish_CI_AS | no |
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

