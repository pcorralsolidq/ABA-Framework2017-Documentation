![SolidQ Logo](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif "Logo Title Text 1")
# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tablas](#head_tablas)
  
* [Vistas](#head_vistas)
  * [bi.authors](#head_bi.authors)
  * [bi.publishers](#head_bi.publishers)
  * [bi.sales](#head_bi.sales)
  * [bi.stores](#head_bi.stores)
  * [bi.titleauthor](#head_bi.titleauthor)
  * [bi.titles](#head_bi.titles)
  

## Info <a name="head_info"></a>
**Abamulti_HLP**

DB Info:
| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| Abamulti_HLP |     300.00 MB| sa| 6| Oct  8 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=852, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 130 |

Files:
| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| Abamulti_HLP_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\Abamulti_HLP_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| Abamulti_HLP_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\Abamulti_HLP_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| Abamulti_HLP_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\Abamulti_HLP_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tablas <a name="head_tablas"></a>


### Vistas <a name="head_vistas"></a>

**bi.authors** <a name="head_bi.authors"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| authors | bi | dbo | 08/10/2017 19:59:01 | 23 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_au_id | varchar | 11 | no | Modern_Spanish_CI_AS | no |
| au_lname | varchar | 40 | no | Modern_Spanish_CI_AS | no |
| au_fname | varchar | 20 | no | Modern_Spanish_CI_AS | no |
| phone | char | 12 | no | Modern_Spanish_CI_AS | no |
| address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |
| contract | bit | 1 | no |  | (n/a) |


Creation SQL Script:
```
CREATE VIEW bi.authors as SELECT [au_id] as pk_au_id

      ,[au_lname]

      ,[au_fname]

      ,[phone]

      ,[address]

      ,[city]

      ,[state]

      ,[zip]

      ,[contract]

  FROM pubs.[dbo].[authors]

```
</br>


**bi.publishers** <a name="head_bi.publishers"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| publishers | bi | dbo | 08/10/2017 19:59:01 | 8 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_pub_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| pub_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | yes | Modern_Spanish_CI_AS | no |


Creation SQL Script:
```


CREATE VIEW bi.publishers as SELECT [pub_id] as pk_pub_id

      ,[pub_name]

      ,[city]

      ,[state]

      ,[country]

  FROM pubs.[dbo].[publishers]

```
</br>


**bi.sales** <a name="head_bi.sales"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| sales | bi | dbo | 08/10/2017 19:59:01 | 21 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| stor_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | no | Modern_Spanish_CI_AS | no |
| incremental | bigint | 8 | yes |  | (n/a) |
| qty | smallint | 2 | no |  | (n/a) |
| payterms | varchar | 12 | no | Modern_Spanish_CI_AS | no |
| title_id | varchar | 6 | no | Modern_Spanish_CI_AS | no |


Creation SQL Script:
```


CREATE VIEW bi.sales as SELECT  CONCAT(stor_id,ord_num,title_id) as pk_id

	  ,[stor_id]

      ,[ord_num] 

      ,CAST([ord_date] as bigint)incremental

      ,[qty]

      ,[payterms]

      ,[title_id]

  FROM pubs.[dbo].[sales]

```
</br>


**bi.stores** <a name="head_bi.stores"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| stores | bi | dbo | 08/10/2017 19:59:01 | 6 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_stor_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| stor_name | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| stor_address | varchar | 40 | yes | Modern_Spanish_CI_AS | no |
| city | varchar | 20 | yes | Modern_Spanish_CI_AS | no |
| state | char | 2 | yes | Modern_Spanish_CI_AS | no |
| zip | char | 5 | yes | Modern_Spanish_CI_AS | no |


Creation SQL Script:
```


CREATE VIEW bi.stores as SELECT [stor_id] as pk_stor_id

      ,[stor_name]

      ,[stor_address]

      ,[city]

      ,[state]

      ,[zip]

  FROM pubs.[dbo].[stores]

```
</br>


**bi.titleauthor** <a name="head_bi.titleauthor"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| titleauthor | bi | dbo | 08/10/2017 19:59:01 | 18 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 17 | no | Modern_Spanish_CI_AS | no |
| au_id | varchar | 11 | no | Modern_Spanish_CI_AS | no |
| title_id | varchar | 6 | no | Modern_Spanish_CI_AS | no |
| au_ord | tinyint | 1 | yes |  | (n/a) |
| royaltyper | int | 4 | yes |  | (n/a) |


Creation SQL Script:
```


CREATE VIEW bi.titleauthor as SELECT CONCAT(au_id,title_id) as pk_id

	  ,[au_id]

      ,[title_id]

      ,[au_ord]

      ,[royaltyper]

  FROM pubs.[dbo].[titleauthor]

```
</br>


**bi.titles** <a name="head_bi.titles"></a>

View info:
| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| titles | bi | dbo | 08/10/2017 19:59:01 | 18 |

Columns:
| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_title_id | varchar | 6 | no | Modern_Spanish_CI_AS | no |
| title | varchar | 80 | no | Modern_Spanish_CI_AS | no |
| type | char | 12 | no | Modern_Spanish_CI_AS | no |
| pub_id | char | 4 | yes | Modern_Spanish_CI_AS | no |
| price | money | 8 | yes |  | (n/a) |
| advance | money | 8 | yes |  | (n/a) |
| royalty | int | 4 | yes |  | (n/a) |
| ytd_sales | int | 4 | yes |  | (n/a) |
| notes | varchar | 200 | yes | Modern_Spanish_CI_AS | no |
| pubdate | datetime | 8 | no |  | (n/a) |


Creation SQL Script:
```


CREATE VIEW bi.titles as SELECT [title_id] as pk_title_id

      ,[title]

      ,[type]

      ,[pub_id]

      ,[price]

      ,[advance]

      ,[royalty]

      ,[ytd_sales]

      ,[notes]

      ,[pubdate]

  FROM pubs.[dbo].[titles]

```
</br>


