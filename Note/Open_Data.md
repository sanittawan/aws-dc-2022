**Optimize data for analysis - AWS open data**
By Peter Schmiedeskamp Statistical and Regulatory Lead, AWS Open Data
goespatial, sustainability and env practices
For providers, can help with hosting, credits

**Assumptions**
1. very large data set (moving data from one geolocation to another can take a long time, so promoting "in-situ" computation)
2. diverse data e.g. in many formats 
3. diverse calculation/computation i.e. cannot apply the same data models to all
4. decoupled compute --> leading to data lake architecture "S3" (alternative = data warehouse esp. tabular data)
5. data with few writes but *many* reads