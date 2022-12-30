# Music-Recommendation-Using-FP-Growth-data-mining-algortihm
In this Project, the association rule data mining (ARM) technique was employed using the Frequent Pattern Growth mining algorithm (FP-Growth) to learn the music listening behavior of listeners in different communities, identify associations among music artists and recommend new music to users

Dataset Description: 
---------------------
The data set is an open dataset from lastfm. Lastfm is a music listening streaming platform. The domain of the dataset is related to music. The data was created and published by the same owners (lastfm). The data is available in a comma separated value (CSV) format and it has a shape of 289955 rows and 4 columns. The names of the 4 attributes are: user_id,  sex,  music_artist,  country.

Methodology: 
-------------
The methodology for this project involved the application of four techniques in big data analytics lifecycle.  The techniques explored are 
1. Data-preprocessing 
2. Exploratory Data Analysis
3. Data visualization
4. Association rule mining (ARM) using FP growth algorithm

The methodology above is implemented programmatically with pyspark i.e python API for Apache Spark framework. Pyspark is employed for this project because it is well suited to handle big data mining tasks due to its flexible, scalable, and fast execution

Data preprocessing
--------------------
A) Removal of duplicates: Two duplicate observations are found in the dataframe. Initially, there are 289955 rows, but after normalization using dropDuplicates ([ ]) function, the number of observation is 289953. The justification for data normalization is to remove duplicates and ensure each observation is a unique row.
___
B) Data Validation: The dataframe is validated to confirm if there is missing data, noisy data or errors in the datatype

Data Exploration / Visualization
--------------------
Numerical transformation such as country-wise distribution, artist wise distribution is perfromed on the dataframe using the grouping method (groupBy) to visually represent these transformations. The insights are graphically represented in the form of bar charts by employing pandas visualization libraries which are Matplotlib and Seaborn

Association Rule mining 
--------
The frequent itemset mining analysis is implemented using FP-Growth machine learning algorithm with weights of 80% train data and 20% test data. The aim of frequent pattern mining is to find all the “interesting rules” that minimum support and confidence threshold that give all possible associations among the frequent music artists. The FP-Growth algorithm was modelled 4 times using four different hyperparameters of minimum support (S) and confidence (C). Each hyperparameterized model was tested using user_id = 154 to evaluate which model has the best music recommendation performance
