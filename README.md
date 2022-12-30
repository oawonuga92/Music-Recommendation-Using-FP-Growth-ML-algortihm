# Music-Recommendation-Using-FP-Growth-algortihm
In this Project, the association rule data mining (ARM) technique was employed using the Frequent Pattern Growth mining algorithm (FP-Growth) to learn the music listening behavior of listeners in different communities, identify associations among music playlist and recommend new music to users

Dataset Description: 
---------------------
The data set is an open dataset from lastfm. Lastfm is a music listening streaming platform. The data was created and published by the same owners. The domain of the dataset is related to music. The data is available in a comma separated value (CSV) format and it has a shape of 289955 rows and 4 columns.

Methodology: 
-------------
The methodology for this project involved application of techniques in big data analytics lifecycle.  The techniques explored are 
1. Data-preprocessing 
2. Exploratory Data Analysis
3. Data visualization
4. Association rule mining (ARM)

Data preprocessing
--------------------
A) Removal of duplicates: Two duplicate observations are in the dataframe. Initially there are 289955 rows, but after normalization using dropDuplicates ([ ]) function, the number of observation is 289953. The justification for data normalization is to remove duplicates and ensure each observation is a unique row.
**
B) Data Validation: The dataframe is validated to confirm if there is missing data, noisy data or errors in the datatype


The methodology is implemented programmatically on with pyspark i.e python API for Apache Spark framework. Pyspark is employed for data exploration actions and transformations because it is well suited to handle big data mining tasks due to its flexible, scalable, and fast execution
