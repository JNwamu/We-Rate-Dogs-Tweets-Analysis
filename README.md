# We-Rate-Dogs-Tweets-Analysis
An analysis performed from the tweet archives of the We Rate dog user.

## Dataset

This Dataset is a tweet archive for the twitter user **@dog_rates** also known as **WeRateDogs**. It is a twitter account that rates people's dog with a comical comment about the dog. The aim of this project is to wrangle it's archive data from 3 different sources to gather a data frame which will then be cleaned and data analysis and visualisation performed for the data. All data gathered from the source has been put here namely **twitter_archive_master**, **image-predictions.tsv** and **tweet_json**

## Summary of Assessment

During the assessing and wrangling process, several quality and untidy issues where identified and cleaned. Below were some of the issues identified.

# Quality Issues


**`twitter_archive_enhanced` table**
- Some tweets containing Retweets are part of the dataframe, original ratings should be used as per specification.
- Original ratings that have images in the expanded url column should also be used as per specification.
- Incomplete and null values for 6 columns namely(in_reply_to_status_id, in_reply_to_user_id,retweeted_status_id,retweeted_status_user_id, retweeted_status_timestamp, expanded_urls).
- Incorrect data type for the timestamp column.
- Incorrect data type for the tweetid column.
- Incorrect name of dog as "a","o" ,"the", "actually" etc in the name column.


 **`image prediction` table**
- lesser data at 2074 than the twitter_archive_enhanced file which is 2356.
- Inconsistent alphabet casing values in the **p1**, **p2** and **p3** columns.
- incorrect data type for the tweet_id column.
- Non descriptive column header.
- Inconsistent decimal places in the prediction confidence columns.


**`twitter API` table**
- lesser data at 2325 than the twitter_archive_enhanced file which is 2356 but more than the image prediction file at 2074
- incorrect data type for tweet_id column.


# Tidness Issues


 **`twitter_archive_enhanced` table**
- various stages(*doggo*, *floofer*, *pupper* and *floofer*) of the dog can be classified under one column in the `twitter_archive_enhanced` table.
- The Source column has some URL before the actual twitter source in the `twitter_archive_enhanced` table.
- Three variables in six columns(**p1,p1_conf,p1_dog, p2,p2_conf,p2_dog,p3,p3_conf,p3_dog**)
- Data in the 3 dataframes are all related to the same object Dog and it's ratings but seperated.


## Key Insights for Visualisation

During the visualisation, commonly used words in the tweets would be seen using the world cloud , we would also validate how efficent the dog prediction algorithm is and also know via which medium twitter user tweets the most amongst other insights dervied from the data. Further interesting insights can be seen in the `act_report`.
