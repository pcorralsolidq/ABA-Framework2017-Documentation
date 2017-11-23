![](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif)

# Aba Framework Documentation
## Database doc

* [Info](#head_info)
* [Tables](#head_tables)
  
* [Views](#head_views)
  * [bi.authors](#bi_authors)
  * [bi.publishers](#bi_publishers)
  * [bi.sales](#bi_sales)
  * [bi.stores](#bi_stores)
  * [bi.titleauthor](#bi_titleauthor)
  * [bi.titles](#bi_titles)
  * [mt.newspapers](#mt_newspapers)
  

## Info <a name='head_info'>
**ABA2017_HLP**

DB Info:

| Name | Size | Owner | id | Created | Status | Compatibility level |
| ---- | ---- | ----- | -- | ------- | ------ | ------------------- |
| ABA2017_HLP |     300.00 MB| sa| 6| Nov  2 2017 | Status=ONLINE, Updateability=READ_WRITE, UserAccess=MULTI_USER, Recovery=SIMPLE, Version=869, Collation=Modern_Spanish_CI_AS, SQLSortOrder=0, IsAutoCreateStatistics, IsAutoUpdateStatistics, IsFullTextEnabled | 140 |

Files:

| Name | id | filename | filegroup | size | maxsize | growth |
| ---- | -- | -------- | --------- | ---- | ------- | ------ |
| ABA2017_HLP_sys | 1 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_HLP_sys.mdf | PRIMARY | 102400 KB | Unlimited | 0 KB |
| ABA2017_HLP_log | 2 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_HLP_log.ldf |  | 102400 KB | 2147483648 KB | 102400 KB |
| ABA2017_HLP_data | 3 | C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\ABA2017_HLP_data.ndf | SECONDARY | 102400 KB | Unlimited | 102400 KB |

### Tables <a name='head_tables'>


### Views <a name='head_views'>

#### bi.authors <a name='head_bi_authors'>

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| authors | bi | dbo | 02/11/2017 14:05:28 | 23 |

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




#### bi.publishers <a name='head_bi_publishers'>

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| publishers | bi | dbo | 02/11/2017 14:05:28 | 8 |

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




#### bi.sales <a name='head_bi_sales'>

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| sales | bi | dbo | 02/11/2017 14:05:28 | 21 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_id | varchar | 30 | no | Modern_Spanish_CI_AS | no |
| stor_id | char | 4 | no | Modern_Spanish_CI_AS | no |
| ord_num | varchar | 20 | no | Modern_Spanish_CI_AS | no |
| ord_date | datetime | 8 | no |  | (n/a) |
| qty | smallint | 2 | no |  | (n/a) |
| payterms | varchar | 12 | no | Modern_Spanish_CI_AS | no |
| title_id | varchar | 6 | no | Modern_Spanish_CI_AS | no |


Creation SQL Script:
```


CREATE VIEW bi.sales as SELECT  CONCAT(stor_id,ord_num,title_id) as pk_id

	,[stor_id]

      ,[ord_num] 

      ,[ord_date]

      ,[qty]

      ,[payterms]

      ,[title_id]

  FROM pubs.[dbo].[sales]

```




#### bi.stores <a name='head_bi_stores'>

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| stores | bi | dbo | 02/11/2017 14:05:28 | 6 |

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




#### bi.titleauthor <a name='head_bi_titleauthor'>

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| titleauthor | bi | dbo | 02/11/2017 14:05:28 | 18 |

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




#### bi.titles <a name='head_bi_titles'>

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| titles | bi | dbo | 02/11/2017 14:05:28 | 18 |

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




#### mt.newspapers <a name='head_mt_newspapers'>

View info:

| View name | Schema | Owner | Creation date | Rows |
| --------- | ------ | ----- | ------------- | ---- |
| newspapers | mt | dbo | 02/11/2017 14:05:28 | 6 |

Columns:

| Columnn name | Type | Length | Nullable | Collation | TrimTrailingBlanks |
| ------------ | ---- | ------ | -------- | --------- | ------------------ |
| pk_np_id | int | 4 | no |  | (n/a) |
| name | varchar | 80 | no | Modern_Spanish_CI_AS | no |
| country | varchar | 30 | no | Modern_Spanish_CI_AS | no |


Creation SQL Script:
```


CREATE VIEW mt.newspapers as SELECT [np_id] as pk_np_id

      ,[name]

	  ,[country]

  FROM newspapers.[dbo].newspapers

```




