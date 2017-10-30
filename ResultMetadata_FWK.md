
![SolidQ Logo](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif "Logo Title Text 1")
# ABA Framework Documentation
* [Home](#head_home)
* [Extraction phase](#head_Extraction_phase)
  * [Loaded tables](#head_Loaded_tables)
  * [Connections](#head_Connections)
  * [Load patterns](#head_Load_patterns)
  * [Data types source vs stg](#head_Data_types)
  * [Source Primary keys](#head_Source_primary_keys)
  * [Active for](#head_active_load_creation_orquestator)
* [Load phase](#head_Load_phase)
  * [Dimensions](#head_dimensions)
  * [Facts](#head_Fact_tables)
  * [SCD](#head_SCD)
  * [Data types source vs dwh](#head_Data_types_source_vs_dwh)
* [Unit Tests](#head_Tests)
* [Log Table](#head_Log)

### Home <a name="head_Home"></a>
Documentation generated using the metadata from ABA2017 database.</br>
_Documentation created: 30/10/2017 18:26:16_

### Extraction phase <a name="head_Extraction_phase"></a>
####  Loaded Tables <a name="head_Loaded_tables"></a>
| Source object schema | Source object name | Destination table schema | Destination table name | Source type id | Helper id |
| -------------------- | ------------------ | ------------------------ | ---------------------- | -------------- | --------- |
| 'bi' | [authors](ResultMetadata_HLP1.md#head_bi.authors) | STG | [authors](ResultMetadata_STG1.md#head_stg.authors) | VIW | 1 |
| 'bi' | [publishers](ResultMetadata_HLP1.md#head_bi.publishers) | STG | [publishers](ResultMetadata_STG1.md#head_stg.publishers) | VIW | 1 |
| 'bi' | [sales](ResultMetadata_HLP1.md#head_bi.sales) | STG | [sales](ResultMetadata_STG1.md#head_stg.sales) | VIW | 1 |
| 'bi' | [stores](ResultMetadata_HLP1.md#head_bi.stores) | STG | [stores](ResultMetadata_STG1.md#head_stg.stores) | VIW | 1 |
| 'bi' | [titleauthor](ResultMetadata_HLP1.md#head_bi.titleauthor) | STG | [titleauthor](ResultMetadata_STG1.md#head_stg.titleauthor) | VIW | 1 |
| 'bi' | [titles](ResultMetadata_HLP1.md#head_bi.titles) | STG | [titles](ResultMetadata_STG1.md#head_stg.titles) | VIW | 1 |
| 'mt' | [newspapers](ResultMetadata_HLP2.md#head_mt.newspapers) | STG | [newspapers](ResultMetadata_STG2.md#head_stg.newspapers) | VIW | 2 |

**Information Source DB:** ABA2017_MD </br>
**Information Source Table:** md.extract_phase_info

[Wiki Extraction Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework)

####  Connections <a name="head_Connections"></a>
| Connection name | Connection string | DB Schemas |
| --------------- | ----------------- | -----------|
| [DWH-1](ResultMetadata_DWH.md) | Data Source=localhost;Initial Catalog=ABA_2017_DWH;Provider=SQLNCLI11.1;Integrated Security=SSPI;Auto Translate=False; | dim,fact |
| [HLP-1](ResultMetadata_HLP1.md) | Provider=SQLNCLI11.1;Data Source=localhost;Initial Catalog=ABA_2017_HLP;Integrated Security=SSPI;Auto Translate=False; | bi,dbo |
| [LOG-1](ResultMetadata_LOG.md) | Data Source=localhost;Initial Catalog=ABA2017_LOG;Provider=SQLNCLI11.1;Integrated Security=SSPI;Auto Translate=False; |  |
| [STG-1](ResultMetadata_STG.md) | Data Source=localhost;Initial Catalog=ABA_2017_STG;Provider=SQLNCLI11.1;Integrated Security=SSPI;Auto Translate=False; | stg,di |
| [HLP-2](ResultMetadata_HLP2.md) | Provider=SQLNCLI11.1;Data Source=localhost;Initial Catalog=ABA_2017_HLP;Integrated Security=SSPI;Auto Translate=False; | mt |
| [STG-2](ResultMetadata_STG.md) | Data Source=localhost;Initial Catalog=ABA_2017_STG2;Provider=SQLNCLI11.1;Integrated Security=SSPI;Auto Translate=False; | stg,di |

**Information Source DB:** ABA2017_MD </br>
**Information Source Table:** md.Connections

####  Load patterns <a name="head_Load_patterns"></a>
| Source object schema | Source object name | Load pattern id | Load pattern |
| -------------------- | ------------------ | --------------- | ------------ |
| bi | [authors](ResultMetadata_HLP1.md#head_bi.authors) | DLH | [Differential Lookup Hash](http://www.solidq.com/wiki/aba/Extraction%20phase.aspx#dlh) |
| bi | [publishers](ResultMetadata_HLP1.md#head_bi.publishers) | DLH | [Differential Lookup Hash](http://www.solidq.com/wiki/aba/Extraction%20phase.aspx#dlh) |
| bi | [sales](ResultMetadata_HLP1.md#head_bi.sales) | DLH | [Differential Lookup Hash](http://www.solidq.com/wiki/aba/Extraction%20phase.aspx#dlh) |
| bi | [stores](ResultMetadata_HLP1.md#head_bi.stores) | DLH | [Differential Lookup Hash](http://www.solidq.com/wiki/aba/Extraction%20phase.aspx#dlh) |
| bi | [titleauthor](ResultMetadata_HLP1.md#head_bi.titleauthor) | DLH | [Differential Lookup Hash](http://www.solidq.com/wiki/aba/Extraction%20phase.aspx#dlh) |
| bi | [titles](ResultMetadata_HLP1.md#head_bi.titles) | DLH | [Differential Lookup Hash](http://www.solidq.com/wiki/aba/Extraction%20phase.aspx#dlh) |
| mt | [newspapers](ResultMetadata_HLP2.md#head_mt.newspapers) | DLH | [Differential Lookup Hash](http://www.solidq.com/wiki/aba/Extraction%20phase.aspx#dlh) |

**Information Source DB:** ABA2017_MD </br>
**Information Source Table:** md.Source_Schema </br>

####  Data types source vs stg <a name="head_Data_types"></a>
| Helper id | Table schema name | Table name | Column name | Destination column name | Data type | Destination data type |
| --------- | ----------------- | ---------- | ----------- | ----------------------- | --------- | --------------------- |
| 1 | bi | authors | address | address | varchar(40) | varchar(40) |
| 1 | bi | authors | au_fname | au_fname | varchar(20) | varchar(20) |
| 1 | bi | authors | au_lname | au_lname | varchar(40) | varchar(40) |
| 1 | bi | authors | city | city | varchar(20) | varchar(20) |
| 1 | bi | authors | contract | contract | bit | bit |
| 1 | bi | authors | phone | phone | char(12) | char(12) |
| 1 | bi | authors | pk_au_id | pk_au_id | varchar(11) | varchar(11) |
| 1 | bi | authors | state | state | char(2) | char(2) |
| 1 | bi | authors | zip | zip | char(5) | char(5) |
| 1 | bi | publishers | city | city | varchar(20) | varchar(20) |
| 1 | bi | publishers | country | country | varchar(30) | varchar(30) |
| 1 | bi | publishers | pk_pub_id | pk_pub_id | char(4) | char(4) |
| 1 | bi | publishers | pub_name | pub_name | varchar(40) | varchar(40) |
| 1 | bi | publishers | state | state | char(2) | char(2) |
| 1 | bi | sales | ord_date | ord_date | datetime | datetime |
| 1 | bi | sales | ord_num | ord_num | varchar(20) | varchar(20) |
| 1 | bi | sales | payterms | payterms | varchar(12) | varchar(12) |
| 1 | bi | sales | pk_id | pk_id | varchar(30) | varchar(30) |
| 1 | bi | sales | qty | qty | smallint | smallint |
| 1 | bi | sales | stor_id | stor_id | char(4) | char(4) |
| 1 | bi | sales | title_id | title_id | varchar(6) | varchar(6) |
| 1 | bi | stores | city | city | varchar(20) | varchar(20) |
| 1 | bi | stores | pk_stor_id | pk_stor_id | char(4) | char(4) |
| 1 | bi | stores | state | state | char(2) | char(2) |
| 1 | bi | stores | stor_address | stor_address | varchar(40) | varchar(40) |
| 1 | bi | stores | stor_name | stor_name | varchar(40) | varchar(40) |
| 1 | bi | stores | zip | zip | char(5) | char(5) |
| 1 | bi | titleauthor | au_id | au_id | varchar(11) | varchar(11) |
| 1 | bi | titleauthor | au_ord | au_ord | tinyint | tinyint |
| 1 | bi | titleauthor | pk_id | pk_id | varchar(17) | varchar(17) |
| 1 | bi | titleauthor | royaltyper | royaltyper | int | int |
| 1 | bi | titleauthor | title_id | title_id | varchar(6) | varchar(6) |
| 1 | bi | titles | advance | advance | money | money |
| 1 | bi | titles | notes | notes | varchar(200) | varchar(200) |
| 1 | bi | titles | pk_title_id | pk_title_id | varchar(6) | varchar(6) |
| 1 | bi | titles | price | price | money | money |
| 1 | bi | titles | pub_id | pub_id | char(4) | char(4) |
| 1 | bi | titles | pubdate | pubdate | datetime | datetime |
| 1 | bi | titles | royalty | royalty | int | int |
| 1 | bi | titles | title | title | varchar(80) | varchar(80) |
| 1 | bi | titles | type | type | char(12) | char(12) |
| 1 | bi | titles | ytd_sales | ytd_sales | int | int |
| 2 | mt | newspapers | country | country | varchar(30) | varchar(30) |
| 2 | mt | newspapers | name | name | varchar(80) | varchar(80) |
| 2 | mt | newspapers | pk_np_id | pk_np_id | int | int |
**Information Source DB:** ABA2017_MD </br>
**Information Source Table:** md.Source_Schema </br>

####  Source Primary Keys <a name="head_Source_primary_keys"></a>
| Source object Schema | Source object name | Primary key columns |
| -------------------- | ------------------ | ------------------- |
| bi |[authors](ResultMetadata_HLP1.md#head_bi.authors) | pk_au_id |
| bi |[publishers](ResultMetadata_HLP1.md#head_bi.publishers) | pk_pub_id |
| bi |[sales](ResultMetadata_HLP1.md#head_bi.sales) | pk_id |
| bi |[stores](ResultMetadata_HLP1.md#head_bi.stores) | pk_stor_id |
| bi |[titleauthor](ResultMetadata_HLP1.md#head_bi.titleauthor) | pk_id |
| bi |[titles](ResultMetadata_HLP1.md#head_bi.titles) | pk_title_id |
| mt |[newspapers](ResultMetadata_HLP2.md#head_mt.newspapers) | pk_np_id |

**Information Source DB:** ABA2017_MD </br>
**Information Source Table:** md.extract_phase_info </br>

[Wiki E Phase naming conventions](http://www.solidq.com/wiki/aba/etl-with-aba-framework#naming)

####  Active for load / creation / orquestator <a name="head_active_load_creation_orquestator"></a>
| Source object schema | Source object name | Active for load | Active for creation | Active for orquestator |
| -------------------- | ------------------ | --------------- | ------------------- | ---------------------- |
| bi | [authors](ResultMetadata_HLP1.md#head_bi.authors) | Y | N | Y
| bi | [publishers](ResultMetadata_HLP1.md#head_bi.publishers) | Y | N | Y
| bi | [sales](ResultMetadata_HLP1.md#head_bi.sales) | Y | N | Y
| bi | [stores](ResultMetadata_HLP1.md#head_bi.stores) | Y | N | Y
| bi | [titleauthor](ResultMetadata_HLP1.md#head_bi.titleauthor) | Y | N | Y
| bi | [titles](ResultMetadata_HLP1.md#head_bi.titles) | Y | N | Y
| mt | [newspapers](ResultMetadata_HLP2.md#head_mt.newspapers) | Y | N | Y

**Information Source DB:** ABA2017_MD </br>
**Information Source Table:** md.extract_phase_info </br>

[Wiki Extraction Phase Info columns](http://www.solidq.com/wiki/aba/framework-databases#epi)

### Load phase <a name="head_Load_phase"></a>
####  Dimensions <a name="head_dimensions"></a>
| Source table name | Destination table name | Active for creation | Active for load | Primary key columns | Detect deletes | Order group |
| ----------------- | ---------------------- | ------------------- | --------------- | ------------------- | -------------- | ----------- |

**Information Source DB:** ABA2017_MD </br>
**Information Source Table:** md.dimension_load_phase_info

[Wiki Loading Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework#loading) </br>
[Wiki Naming Conventions Loading Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework#naming-loading)

####  Fact tables <a name="head_Fact_tables"></a>
| Source table name | Destination table name | Active for creation | Active for load | Primary key columns | Detect deletes | Order group |
| ----------------- | ---------------------- | ------------------- | --------------- | ------------------- | -------------- | ----------- |
| [vw_fact_sales](ResultMetadata_STG1.md#head_etl.vw_fact_sales) | [sales](ResultMetadata_DWH1.md#head_dim.sales) | N | Y | idsales | Y | 1 |

**Information Source DB:** ABA2017_MD </br>
**Information Source Table:** md.load_phase_info

[Wiki Loading Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework#loading) </br>
[Wiki Naming Conventions Loading Phase](http://www.solidq.com/wiki/aba/etl-with-aba-framework#naming-loading)

####  SCD <a name="head_SCD"></a>
| Source table name | Destination column name | Change type | Type description |
| ----------------- | ----------------------- | ----------- | ---------------- |


**Information Source DB:** ABA2017_MD </br>
**Information Source Table:** md.dimensions_load_phase_info_columns

[Wiki Slowly Change Dimensions](http://www.solidq.com/wiki/aba/etl-with-aba-framework#scd)

####  Data types source vs dwh <a name="head_Data_types_source_vs_dwh"></a>
Under construction

### Unit Tests <a name="head_Tests"></a>
| Execution id | Test name  | Start date | End date | Result | Message |
| ------------ | ---------- | ---------- | -------- | ------ | ------- |


#### Test Results


[Wiki Unit Tests](http://www.solidq.com/wiki/aba/automatedtesting/#main_characteristics)

### Log Table <a name="head_Log"></a>
| Schema name | Table name | Type | Start date | End date | Status | Loaded by | Inserted rows | Updated rows | Deleted rows |
| ----------- | ---------- | ---- | ---------- | -------- | ------ | --------- | ------------- | ------------ | ------------ |
| DWH | sales | F | 26/10/2017 16:54:58 | 26/10/2017 16:54:59 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 | <deleted_rows>0 |
| DWH | publisher | I | 26/10/2017 16:54:54 | 26/10/2017 16:54:58 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>8 | <updated_rows>0 | <deleted_rows>0 |
| DWH | author | I | 26/10/2017 16:54:54 | 26/10/2017 16:54:58 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>23 | <updated_rows>0 | <deleted_rows>0 |
| DWH | store | I | 26/10/2017 16:54:54 | 26/10/2017 16:54:58 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| DWH | title | I | 26/10/2017 16:54:54 | 26/10/2017 16:54:58 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>18 | <updated_rows>0 | <deleted_rows>0 |
| dwh | OrquestadorDWH PubsOffice | F | 26/10/2017 16:54:53 | 26/10/2017 16:54:59 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| DWH | newspapers | I | 26/10/2017 16:54:46 | 26/10/2017 16:54:47 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| dwh | OrquestadorDWH Marketing | F | 26/10/2017 16:54:46 | 26/10/2017 16:54:47 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| DWH | sales | F | 26/10/2017 16:52:26 | 26/10/2017 16:52:27 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>23 | <updated_rows>0 | <deleted_rows>0 |
| DWH | title | I | 26/10/2017 16:52:22 | 26/10/2017 16:52:25 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>18 | <updated_rows>0 | <deleted_rows>0 |
| DWH | author | I | 26/10/2017 16:52:22 | 26/10/2017 16:52:25 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>23 | <updated_rows>0 | <deleted_rows>0 |
| DWH | store | I | 26/10/2017 16:52:22 | 26/10/2017 16:52:25 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| DWH | publisher | I | 26/10/2017 16:52:21 | 26/10/2017 16:52:25 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>8 | <updated_rows>0 | <deleted_rows>0 |
| dwh | OrquestadorDWH PubsOffice | F | 26/10/2017 16:52:21 | 26/10/2017 16:52:27 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| DWH | newspapers | I | 26/10/2017 16:52:14 | 26/10/2017 16:52:15 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 | <deleted_rows>0 |
| dwh | OrquestadorDWH Marketing | F | 26/10/2017 16:52:14 | 26/10/2017 16:52:15 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| DWH | newspapers | I | 26/10/2017 16:45:11 | 26/10/2017 16:45:12 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| dwh | OrquestadorDWH Marketing | F | 26/10/2017 16:45:10 | 26/10/2017 16:45:12 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| stg | newspapers | I | 26/10/2017 13:56:07 | 26/10/2017 13:56:08 | F | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| stg |  Marketing | I | 26/10/2017 13:56:06 | 26/10/2017 13:56:08 | F | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| DWH | title | I | 26/10/2017 13:25:56 | 26/10/2017 13:25:59 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>18 | <updated_rows>0 | <deleted_rows>0 |
| DWH | author | I | 26/10/2017 13:25:56 | 26/10/2017 13:25:59 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>23 | <updated_rows>0 | <deleted_rows>0 |
| DWH | publisher | I | 26/10/2017 13:25:56 | 26/10/2017 13:25:59 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>8 | <updated_rows>0 | <deleted_rows>0 |
| DWH | store | I | 26/10/2017 13:25:56 | 26/10/2017 13:25:59 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| dwh | OrquestadorDWH PubsOffice | F | 26/10/2017 13:25:54 | 26/10/2017 13:25:59 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| DWH | newspapers | I | 26/10/2017 13:25:11 | 26/10/2017 13:25:12 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>6 | <updated_rows>0 | <deleted_rows>0 |
| dwh | OrquestadorDWH Marketing | F | 26/10/2017 13:25:10 | 26/10/2017 13:25:12 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| dwh | OrquestadorDWH Marketing | F | 26/10/2017 13:12:18 | 01/01/0001 0:00:00 |  | MicrosoftAccount\pcl23ua@gmail.com |  |  |  |
| dwh | OrquestadorDWH Marketing | F | 26/10/2017 13:10:26 | 01/01/0001 0:00:00 |  | MicrosoftAccount\pcl23ua@gmail.com |  |  |  |
| stg | newspapers | F | 26/10/2017 12:55:35 | 26/10/2017 12:55:35 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>6 | <updated_rows>0 |  |
| stg | stores | F | 26/10/2017 12:43:49 | 26/10/2017 12:43:52 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>6 | <updated_rows>0 |  |
| stg | titles | F | 26/10/2017 12:43:49 | 26/10/2017 12:43:52 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>18 | <updated_rows>0 |  |
| stg | publishers | F | 26/10/2017 12:43:49 | 26/10/2017 12:43:52 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>8 | <updated_rows>0 |  |
| stg | authors | F | 26/10/2017 12:43:48 | 26/10/2017 12:43:52 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>23 | <updated_rows>0 |  |
| stg | titleauthor | F | 26/10/2017 12:43:48 | 26/10/2017 12:43:52 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>18 | <updated_rows>0 |  |
| stg | sales | F | 26/10/2017 12:43:48 | 26/10/2017 12:43:52 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>21 | <updated_rows>0 |  |
| stg |  PubsOffice | I | 26/10/2017 12:43:48 | 26/10/2017 12:43:52 | S | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| stg |  Marketing | I | 26/10/2017 12:40:37 | 26/10/2017 12:40:37 | F | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| stg |  Marketing | I | 26/10/2017 12:33:05 | 26/10/2017 12:33:05 | F | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |
| stg |  Marketing | I | 26/10/2017 12:29:47 | 26/10/2017 12:29:48 | F | MicrosoftAccount\pcl23ua@gmail.com | <inserted_rows>0 | <updated_rows>0 |  |


[Wiki LOG Database](http://www.solidq.com/wiki/aba/framework-databases#log-database)