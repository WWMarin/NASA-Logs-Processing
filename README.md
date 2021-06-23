# NASA Logs Processing
This is an example project of cleaning and analysing data with Spark SQL    
The challenge consists of answering the following questions:  
  
- Number of unique hosts  
- Total number of 404 errors  
- The 5 URLs that caused the most 404 errors  
- Number of daily 404 errors  
- Total bytes returned  
  
Official dataset source:  
https://ita.ee.lbl.gov/html/contrib/NASA-HTTP.html  
  
Data:  
ftp://ita.ee.lbl.gov/traces/NASA_access_log_Jul95.gz  
ftp://ita.ee.lbl.gov/traces/NASA_access_log_Aug95.gz  

About the dataset:  
The dataset holds all the HTTP requests to the server at NASA'S Kennedy Space Center for July and August of 1995. 

### View the Jupyter Notebook online with [nbviewer](https://nbviewer.jupyter.org/github/WWMarin/NASA-Logs-Processing/blob/main/nasa_logs_processing.ipynb) or [Binder](https://mybinder.org/v2/gh/WWMarin/NASA-Logs-Processing/main?filepath=nasa_logs_processing.ipynb)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/WWMarin/NASA-Logs-Processing/main?filepath=nasa_logs_processing.ipynb)

## Data
|                host|rfc931|username| date_time_timezone|             request|statuscode|bytes|
|--------------------|------|--------|-------------------|--------------------|----------|-----|
|        199.72.81.55|     -|       -|1995-07-01 01:00:01|GET /history/apol...|       200| 6245|
|unicomp6.unicomp.net|     -|       -|1995-07-01 01:00:06|GET /shuttle/coun...|       200| 3985|
|      199.120.110.21|     -|       -|1995-07-01 01:00:09|GET /shuttle/miss...|       200| 4085|
|  burger.letters.com|     -|       -|1995-07-01 01:00:11|GET /shuttle/coun...|       304|    0|
|      199.120.110.21|     -|       -|1995-07-01 01:00:11|GET /shuttle/miss...|       200| 4179|
|  burger.letters.com|     -|       -|1995-07-01 01:00:12|GET /images/NASA-...|       304|    0|
|  burger.letters.com|     -|       -|1995-07-01 01:00:12|GET /shuttle/coun...|       200|    0|
|     205.212.115.106|     -|       -|1995-07-01 01:00:12|GET /shuttle/coun...|       200| 3985|
|         d104.aa.net|     -|       -|1995-07-01 01:00:13|GET /shuttle/coun...|       200| 3985|

*only showing top 9 rows*

### Number of Unique Hosts
|Unique_Hosts|
|------------|
|      137979|

### Total Number of 404 Errors
|404_Errors|
|----------|
|     20638|

### The 5 URLs that Caused the Most 404 Errors
|                host|404_Errors|
|--------------------|----------|
|hoohoo.ncsa.uiuc.edu|       251|
|piweba3y.prodigy.com|       157|
|jbiagioni.npt.nuw...|       132|
|piweba1y.prodigy.com|       114|
|www-d4.proxy.aol.com|        91|

### Number of Daily 404 Errors
| date_time_timezone|404_Errors|
|-------------------|----------|
|1995-08-11 13:05:59|         7|
|1995-08-28 12:56:35|         7|
|1995-08-11 13:05:58|         5|
|1995-07-12 11:35:09|         5|
|1995-07-12 11:20:43|         5|
|1995-08-17 17:55:00|         5|
|1995-07-12 11:24:50|         5|
|1995-07-12 11:35:12|         5|
|1995-08-28 18:14:32|         5|

*only showing top 9 rows*

### Total Bytes Returned
|      Bytes|
|-----------|
|65136540452|
