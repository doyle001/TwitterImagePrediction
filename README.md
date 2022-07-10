Twitter Image Prediction
Project Objectives
The Project main Objectives were:

- Perform data wrangling (gathering, assessing and cleaning) on provided thee sources of data
- Store, analyze, and visualize the wrangled data.
- Reporting on (1) data wrangling efforts and (2) data analyses and visualizations
1.0 Gathering Data
In this phase, the three pieces of data were gathered and represented as pandas dataframes:
- The WeRateDogs Twitter archive (file on hand, manual download of 'twitter-archiveenhanced.csv')
- The tweet image predictions ('image-predictions.tsv'). This file was be downloaded programmatically using the Requests library from a provided URL.
- Each tweet's entire set of JSON data (with at minimum tweet ID, retweet count, and favorite count) in a file called 'tweet_json.txt' were stored using Twitter API andPython's Tweepy library. Each tweet's JSON data was written to its own line.
2.0 and 3.0: Assessing and Cleaning Data
While working with data, a number of observations were made. Below are the observations along with actions taken in the Cleaning Step

twitter_archive
Some values in rating_denominator column isn't "10" were fixed
Some values in rating_numerator column more than "15" were fixed
timestamp were "data time" not "str"
retweeted_status_id were removed because we interest in tweet
retweeted_status_timestamp should be removed because we interest in tweet
image_predictions
Drop all records for non dogs from image_predictions_clean dataframe as we only interested in dogs rating
Removed unnecessary columns
Rename columns of image_predictions_clean data frame to be more descriptive
Json_data
Fixed name for "id" column in json_data_clean to "tweet_id" to be consistent with other two data frames while merging
