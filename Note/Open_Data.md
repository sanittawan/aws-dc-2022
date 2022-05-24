**Optimize data for analysis - AWS open data**
By Peter Schmiedeskamp Statistical and Regulatory Lead, AWS Open Data
goespatial, sustainability and env practices
For providers, can help with hosting, credits

**Assumptions and first principle**
1. very large data set (moving data from one geolocation to another can take a long time, so promoting "in-situ" computation)
2. diverse data e.g. in many formats 
3. diverse calculation/computation i.e. cannot apply the same data models to all
4. decoupled compute --> leading to data lake architecture "S3" (alternative = data warehouse esp. tabular data)
5. data with few writes but *many* reads
6. minimize data access

**Services**  
Notebook [link](https://github.com/pschmied/opn201/blob/main/opn201-data-optimization-cheatsheet.ipynb)  
*S3*
- support concurrency (allowing many users to use it with stability)
- scalability  

- too small objects leads to too many requests and listing of all objects will take time (unless have way to bucket data)
- too big leads to downloading more data than needed (check out AWS select)
- recommend using hive style naming conventions e.g. "type=mobile" "year=2021" can think of it as a column in a tabular data set
- zipfiles are not recommended for optimization. If tabular, use Parquet and ORC. The goal is to choose a format that accommodates range request

*Athena*
- tabular data which needs data, schema, and index
- cvs vs orc. the difference is that csv is arranged in row format. If you need 2 columns, Athena still needs to read all rows to grab the 2 columns. By contrast, ORC or Parquet is column-based, arranged by columns. So Athena can just read only the two columns that are needed. Good for optimization
- "create table as" in Athena (c as query). getting Athena to get a part of the csv file to write to a csv file
- geospatial format 
  
Last points
- array data with linear algebra operations --> check out zar
- aws skill builder and certifications 