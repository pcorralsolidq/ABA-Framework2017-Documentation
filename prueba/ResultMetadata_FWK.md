
![](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif)

# ABA Framework Documentation
* [Home](#home)
* [Extraction phase](#head_extraction_phase)
  * [Loaded tables](#head_loaded_tables)
  * [Connections](#head_connections)
  * [Load patterns](#head_load_patterns)
  * [Data types source vs stg](#head_data_types_source_vs_stg)
  * [Source Primary keys](#head_source_primary_keys)
  * [Active for](#head_active_for)
* [Load phase](#head_load_phase)
  * [Dimensions](#head_dimensions)
  * [Fact tables](#head_fact_tables)
  * [SCD](#head_scd)
* [Unit Tests](#head_unit_tests)
* [Log Table](#head_log_table)

### Home
Documentation generated using the metadata from ABA2017 database.

_Documentation created: 23/11/2017 16:31:24_

### Extraction phase <a name='head_extraction_phase'>
####  Loaded Tables <a name='head_loaded_tables'>
| Source object schema | Source object name | Destination table schema | Destination table name | Source type id | Helper id |
| -------------------- | ------------------ | ------------------------ | ---------------------- | -------------- | --------- |
| 'dbo' | [cdc_states](ResultMetadata_HLP3.md#dbo.cdc_states) | STG | [cdc_states](ResultMetadata_STG1.md#stg.cdc_states) | VIW | 3 |
| 'dbo' | [systranschemas](ResultMetadata_HLP3.md#dbo.systranschemas) | STG | [systranschemas](ResultMetadata_STG1.md#stg.systranschemas) | VIW | 3 |
| 'dbo' | [writers](ResultMetadata_HLP3.md#dbo.writers) | STG | [writers](ResultMetadata_STG1.md#stg.writers) | VIW | 3 |
| 'dbo' | [employee](ResultMetadata_HLP4.md#dbo.employee) | STG | [employee](ResultMetadata_STG2.md#stg.employee) | VIW | 4 |

**Information Source DB:** ABA2017_MD

**Information Source Table:** md.extract_phase_info

[Wiki Extraction Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework)

####  Connections <a name='head_connections'>
| Connection name | Connection string | DB Schemas |
| --------------- | ----------------- | -----------|
| [DWH-1](ResultMetadata_DWH1.md) | Data Source=localhost;Initial Catalog=ABA2017_DWH;Provider=SQLNCLI11.1;Integrated Security=SSPI;Auto Translate=False; | dim,fact |
| [HLP-1](ResultMetadata_HLP1.md) | Provider=SQLNCLI11.1;Data Source=localhost;Initial Catalog=ABA2017_HLP;Integrated Security=SSPI;Auto Translate=False; | bi |
| [LOG-1](ResultMetadata_LOG.md) | Data Source=localhost;Initial Catalog=ABA2017_LOG;Provider=SQLNCLI11.1;Integrated Security=SSPI;Auto Translate=False; |  |
| [STG-1](ResultMetadata_STG1.md) | Data Source=localhost;Initial Catalog=ABA2017_STG;Provider=SQLNCLI11.1;Integrated Security=SSPI;Auto Translate=False; | stg,di |
| [HLP-2](ResultMetadata_HLP2.md) | Provider=SQLNCLI11.1;Data Source=localhost;Initial Catalog=ABA2017_HLP;Integrated Security=SSPI;Auto Translate=False; | mt |
| [STG-2](ResultMetadata_STG2.md) | Data Source=localhost;Initial Catalog=ABA2017_STG2;Provider=SQLNCLI11.1;Integrated Security=SSPI;Auto Translate=False; | stg,di |
| [HLP-3](ResultMetadata_HLP3.md) | Provider=SQLNCLI11.1;Data Source=localhost;Initial Catalog=CDC_Demo;Integrated Security=SSPI;Auto Translate=False; | dbo |
| [HLP-4](ResultMetadata_HLP4.md) | Provider=SQLNCLI11.1;Data Source=localhost;Initial Catalog=CTC_Demo;Integrated Security=SSPI;Auto Translate=False; | dbo |

**Information Source DB:** ABA2017_MD

**Information Source Table:** md.Connections

####  Load patterns <a name='head_load_patterns'>
| Source object schema | Source object name | Load pattern id | Load pattern |
| -------------------- | ------------------ | --------------- | ------------ |
| dbo | [cdc_states](ResultMetadata_HLP3.md#dbo.cdc_states) | DLH | [Differential Lookup Hash](http://www.solidq.com/wiki/aba/etl-with-aba-framework#dlh) |
| dbo | [systranschemas](ResultMetadata_HLP3.md#dbo.systranschemas) | DLH | [Differential Lookup Hash](http://www.solidq.com/wiki/aba/etl-with-aba-framework#dlh) |
| dbo | [writers](ResultMetadata_HLP3.md#dbo.writers) | CDC | [Change Data Capture](http://www.solidq.com/wiki/aba/etl-with-aba-framework#cdc) |
| dbo | [employee](ResultMetadata_HLP4.md#dbo.employee) | CTC | [Change Tracking Pattern](http://www.solidq.com/wiki/aba/etl-with-aba-framework#ctc) |

**Information Source DB:** ABA2017_MD

**Information Source Table:** md.Source_Schema

####  Data types source vs stg <a name='head_data_types_source_vs_stg'>
| Helper id | Table schema name | Table name | Column name | Destination column name | Data type | Destination data type |
| --------- | ----------------- | ---------- | ----------- | ----------------------- | --------- | --------------------- |
| 3 | dbo | cdc_states | name | name | nvarchar(256) | nvarchar(256) |
| 3 | dbo | cdc_states | state | state | nvarchar(256) | nvarchar(256) |
| 3 | dbo | systranschemas | endlsn | endlsn | binary | binary |
| 3 | dbo | systranschemas | startlsn | startlsn | binary | binary |
| 3 | dbo | systranschemas | tabid | tabid | int | int |
| 3 | dbo | systranschemas | typeid | typeid | int | int |
| 3 | dbo | writers | address | address | nvarchar(40) | nvarchar(40) |
| 3 | dbo | writers | au_fname | au_fname | nvarchar(20) | nvarchar(20) |
| 3 | dbo | writers | au_id | au_id | nvarchar(50) | nvarchar(50) |
| 3 | dbo | writers | au_lname | au_lname | nvarchar(40) | nvarchar(40) |
| 3 | dbo | writers | city | city | nvarchar(20) | nvarchar(20) |
| 3 | dbo | writers | contract | contract | bit | bit |
| 3 | dbo | writers | phone | phone | nchar(12) | nchar(12) |
| 3 | dbo | writers | state | state | nchar(2) | nchar(2) |
| 3 | dbo | writers | zip | zip | nchar(5) | nchar(5) |
| 4 | dbo | employee | emp_id | emp_id | varchar(50) | varchar(50) |
| 4 | dbo | employee | fname | fname | varchar(20) | varchar(20) |
| 4 | dbo | employee | hire_date | hire_date | datetime | datetime |
| 4 | dbo | employee | job_id | job_id | smallint | smallint |
| 4 | dbo | employee | job_lvl | job_lvl | tinyint | tinyint |
| 4 | dbo | employee | lname | lname | varchar(30) | varchar(30) |
| 4 | dbo | employee | minit | minit | char(1) | char(1) |
| 4 | dbo | employee | pub_id | pub_id | char(4) | char(4) |
**Information Source DB:** ABA2017_MD

**Information Source Table:** md.Source_Schema

####  Source Primary Keys <a name='head_source_primary_keys'>
| Source object Schema | Source object name | Primary key columns |
| -------------------- | ------------------ | ------------------- |
| dbo |[cdc_states](ResultMetadata_HLP3.md#dbo.cdc_states) |  |
| dbo |[systranschemas](ResultMetadata_HLP3.md#dbo.systranschemas) |  |
| dbo |[writers](ResultMetadata_HLP3.md#dbo.writers) |  |
| dbo |[employee](ResultMetadata_HLP4.md#dbo.employee) | emp_id |

**Information Source DB:** ABA2017_MD

**Information Source Table:** md.extract_phase_info

[Wiki E Phase naming conventions](http://www.solidq.com/wiki/aba/etl-with-aba-framework#naming)

####  Active for load creation orquestator <a name='head_active_for'>
| Source object schema | Source object name | Active for load | Active for creation | Active for orquestator |
| -------------------- | ------------------ | --------------- | ------------------- | ---------------------- |
| dbo | [cdc_states](ResultMetadata_HLP3.md#dbo.cdc_states) | Y | Y | Y
| dbo | [systranschemas](ResultMetadata_HLP3.md#dbo.systranschemas) | Y | Y | Y
| dbo | [writers](ResultMetadata_HLP3.md#dbo.writers) | Y | N | Y
| dbo | [employee](ResultMetadata_HLP4.md#dbo.employee) | Y | N | Y

**Information Source DB:** ABA2017_MD

**Information Source Table:** md.extract_phase_info

[Wiki Extraction Phase Info columns](http://www.solidq.com/wiki/aba/framework-databases#epi)

### Load phase <a name='head_load_phase'>
####  Dimensions <a name='head_dimensions'>
| Source table name | Destination table name | Active for creation | Active for load | Primary key columns | Detect deletes | Order group |
| ----------------- | ---------------------- | ------------------- | --------------- | ------------------- | -------------- | ----------- |

**Information Source DB:** ABA2017_MD

**Information Source Table:** md.dimension_load_phase_info

[Wiki Loading Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework#loading)

[Wiki Naming Conventions Loading Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework#naming-loading)

####  Fact tables <a name='head_fact_tables'>
| Source table name | Destination table name | Active for creation | Active for load | Primary key columns | Detect deletes | Order group |
| ----------------- | ---------------------- | ------------------- | --------------- | ------------------- | -------------- | ----------- |
| [vw_fact_sales](ResultMetadata_STG1.md#etl.vw_fact_sales) | [sales](ResultMetadata_DWH1.md#dim.sales) | N | Y | idsales | Y | 1 |

**Information Source DB:** ABA2017_MD

**Information Source Table:** md.load_phase_info

[Wiki Loading Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework#loading)

[Wiki Naming Conventions Loading Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework#naming-loading)

####  SCD <a name='head_scd'>
| Source table name | Destination column name | Change type | Type description |
| ----------------- | ----------------------- | ----------- | ---------------- |


**Information Source DB:** ABA2017_MD

**Information Source Table:** md.dimensions_load_phase_info_columns

[Wiki Slowly Change Dimensions](http://www.solidq.com/wiki/aba/etl-with-aba-framework#scd)


### Unit Tests <a name='head_unit_tests'>
| Execution id | Test name  | Start date | End date | Result | Message |
| ------------ | ---------- | ---------- | -------- | ------ | ------- |
| 1 | NBi.NUnit.Runtime.TestSuite.Source.Helper.PK .Persons.HLP-1.STG-1 | 04/10/2017 9:19:01 | 01/01/0001 0:00:00 | Error | [See message](#head_test_1) | 
| 1 | NBi.NUnit.Runtime.TestSuite.Source.Helper.PK .authors.HLP-1.STG-1 | 04/10/2017 9:19:01 | 01/01/0001 0:00:00 | Success |  | |
| 1 | NBi.NUnit.Runtime.TestSuite.Source.Helper.ERR.authors.HLP-1.STG-1 | 04/10/2017 9:19:01 | 01/01/0001 0:00:00 | Success |  | |


#### Test Results

##### Test 1 <'head_test_1'>
NBi.NUnit.Runtime.CustomStackTraceAssertionException : Execution of the query doesnt match the expected result 

  Expected: 
ResultSet with 0 row

This result set is empty.


  But was:  
ResultSet with 2 rows

     KEY (Text)
     ---------- 
     1         
     2         



Unexpected rows:
----------------

ResultSet with 2 rows

     KEY (Text)
     ---------- 
     1         
     2         










[Wiki Unit Tests](http://www.solidq.com/wiki/aba/automatedtesting/#main_characteristics)

### Log Table <a name='head_log_table'>
| Schema name | Table name | Type | Start date | End date | Status | Loaded by | Inserted rows | Updated rows | Deleted rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| stg | employee | I | 16/11/2017 16:14:47 | 16/11/2017 16:14:48 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>0 | <updated_rows>0 | <deleted_rows>1 |
| stg | employee | I | 16/11/2017 16:05:11 | 16/11/2017 16:05:12 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>43 | <updated_rows>0 | <deleted_rows>0 |
| stg | writers | F | 13/11/2017 9:21:28 | 13/11/2017 9:21:28 | S | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 9:20:32 | 13/11/2017 9:20:32 | S | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 9:19:02 | 13/11/2017 9:19:02 | S | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 9:18:03 | 13/11/2017 9:18:04 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 9:17:31 | 13/11/2017 9:17:31 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | writers | F | 13/11/2017 8:53:07 | 13/11/2017 8:53:08 | S | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 16:44:48 | 09/11/2017 16:44:48 | S | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 16:07:58 | 09/11/2017 16:07:58 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 16:05:18 | 09/11/2017 16:05:19 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 16:04:54 | 09/11/2017 16:04:54 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 16:04:26 | 09/11/2017 16:04:26 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 15:59:04 | 09/11/2017 15:59:04 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 15:58:05 | 09/11/2017 15:58:06 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 15:57:01 | 09/11/2017 15:57:01 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 15:56:28 | 09/11/2017 15:56:29 | F | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| stg | autores | F | 09/11/2017 14:27:01 | 09/11/2017 14:27:01 | S | DESKTOP-HCA06TJ\\Pablo Corral |  |  |  |
| DWH | sales | F | 02/11/2017 15:57:21 | 02/11/2017 15:57:23 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>23 | <updated_rows>0 | <deleted_rows>0 |
| DWH | store | I | 02/11/2017 15:57:17 | 02/11/2017 15:57:20 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| DWH | title | I | 02/11/2017 15:57:17 | 02/11/2017 15:57:20 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>18 | <updated_rows>0 | <deleted_rows>0 |
| DWH | publisher | I | 02/11/2017 15:57:17 | 02/11/2017 15:57:20 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>8 | <updated_rows>0 | <deleted_rows>0 |
| DWH | author | I | 02/11/2017 15:57:17 | 02/11/2017 15:57:20 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>23 | <updated_rows>0 | <deleted_rows>0 |
| dwh | OrquestadorDWH PubsOffice | F | 02/11/2017 15:57:16 | 02/11/2017 15:57:23 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>0 | <updated_rows>0 |  |
| DWH | newspapers | I | 02/11/2017 15:57:08 | 02/11/2017 15:57:09 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| dwh | OrquestadorDWH Marketing | F | 02/11/2017 15:57:08 | 02/11/2017 15:57:09 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>0 | <updated_rows>0 |  |
| stg | titles | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>18 | <updated_rows>0 | <deleted_rows>0 |
| stg | authors | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>23 | <updated_rows>0 | <deleted_rows>0 |
| stg | stores | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| stg | titleauthor | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>18 | <updated_rows>0 | <deleted_rows>0 |
| stg | sales | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>21 | <updated_rows>0 | <deleted_rows>0 |
| stg | publishers | I | 02/11/2017 15:52:00 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>8 | <updated_rows>0 | <deleted_rows>0 |
| stg |  PubsOffice | I | 02/11/2017 15:51:59 | 02/11/2017 15:52:06 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>0 | <updated_rows>0 |  |
| stg | newspapers | I | 02/11/2017 15:51:51 | 02/11/2017 15:51:52 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| stg |  Marketing | I | 02/11/2017 15:51:50 | 02/11/2017 15:51:52 | S | DESKTOP-HCA06TJ\\Pablo Corral | <inserted_rows>0 | <updated_rows>0 |  |


[Wiki LOG Database](http://www.solidq.com/wiki/aba/framework-databases#log-database)