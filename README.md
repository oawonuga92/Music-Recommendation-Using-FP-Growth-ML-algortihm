# Music-Recommendation-Using-FP-Growth-data-mining-algortihm
In this Project, the association rule data mining (ARM) technique was employed using the Frequent Pattern Growth algorithm (FP-Growth) to learn the music listening behavior of listeners in different communities, identify associations among music artists and recommend new music to users

I. Dataset Description: 
---------------------
The data set is an open dataset from lastfm. Lastfm is a music listening streaming platform. The domain of the dataset is related to music. The data was created and published by the same owners (lastfm). The data is available in a comma separated value (CSV) format and it has a shape of 289955 rows and 4 columns. The names of the 4 attributes are: user_id,  sex,  music_artist,  country.

II. Methodology: 
-------------
The methodology for this project involved the application of four techniques in big data analytics lifecycle.  The techniques explored are 
1. Data-preprocessing 
2. Exploratory Data Analysis
3. Data visualization
4. Association rule mining (ARM) using FP growth algorithm

The methodology above is implemented programmatically on Google Colab platfrom with pyspark i.e python API for Apache Spark framework. Pyspark is employed for this project because it is well suited to handle big data mining tasks due to its flexible, scalable, and fast execution

a. Data preprocessing
--------------------
i) Removal of duplicates: Two duplicate observations are found in the dataframe. Initially, there are 289955 rows, but after normalization using dropDuplicates ([ ]) function, the number of observation is 289953. The justification for data normalization is to remove duplicates and ensure each observation is a unique row.
___
ii) Data Validation: The dataframe is validated to confirm if there is missing data, noisy data or errors in the datatype

b. Data Exploration / Visualization
--------------------
Numerical transformation such as country-wise distribution, artist wise distribution is perfromed on the dataframe using the grouping method (groupBy). These transformations are graphically represented in the form of bar charts by employing pandas visualization libraries which are Matplotlib and Seaborn

III. Association Rule mining 
--------
The frequent itemset mining analysis is implemented using FP-Growth machine learning algorithm with weights of 80% train data and 20% test data. The aim of frequent pattern mining is to find all the “interesting rules” that minimum support and confidence threshold that give all possible associations among the frequent music artists. The FP-Growth algorithm was modelled 4 times using four different hyperparameters of minimum support (S) and confidence (C). Each hyperparameterized model was tested using user_id = 154 to evaluate which model has the best music recommendation performance.

IV. Results / Conclusion
--------------
From the music prediction results of user 154, it was observed that only the 3rd and 4th hyperparameterized FP-Growth models recommended hip-hop music artists for the user based on the user’s listening history. Model 1 and 2 did not recommend any music artist for the listener even though the support and confidence value were set to recommended values based according to scholars. 
____
Model 3 provided two recommendations, however, both recommendations were only hip-hop artists. Despite model 3 having the highest number of association rules and frequent itemsets, it was unable to make more interesting recommendations 
___
In contrast, The 4th hyperparameterized model showed more promising predictions than the other three parameterized models. Model 4 recommended five hip-hop musicians (t.i, eminem, kanye west, 2-pac, jay-z), two rock musicians (coldplay and radiohead), and one reggae music artist (the killers). Model 4 is the best fit recommendation model because it was able to find more interesting rules that give possible relationships among music artists. 

