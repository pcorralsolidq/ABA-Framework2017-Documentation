![](http://www.solidq.com/wp-content/uploads/2015/06/Logo-SolidQ-Web.gif)

# ABA Framework Last Test Execution


## Warning!
Se han encontrado 1 errores.


| test_name | start_date | end_date | result | executed | message |
| --------- | ---------- | -------- | ------ | -------- | ------- |
| NBi.NUnit.Runtime.TestSuite.Source.Helper.PK .Persons.HLP-1.STG-1 | 04/10/2017 9:19:01 | 01/01/0001 0:00:00 | Error | True | [See message](#head_test_1) | 
| NBi.NUnit.Runtime.TestSuite.Source.Helper.PK .authors.HLP-1.STG-1 | 04/10/2017 9:19:01 | 01/01/0001 0:00:00 | Success | True |  | |
| NBi.NUnit.Runtime.TestSuite.Source.Helper.ERR.authors.HLP-1.STG-1 | 04/10/2017 9:19:01 | 01/01/0001 0:00:00 | Success | True |  | |

#### Test Results

##### Test 1 {#head_test_1}
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









