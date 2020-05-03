# STA9760-Yelp-Reviews-Project
This project is to analyze a subset of Yelp's business, reviews and user data (~10G), using Spark on AWS EMR. This dataset comes to me from Kaggle although I have taken steps to pull this data into a s3 bucket: s3://sta9760-yelp-reviews/*business.json.

## [Analysis](https://github.com/yb19/STA9760-Yelp-Reviews-Project/blob/master/Analysis.ipynb)

First, I configurate the cluster and notebook on AWS EMR (configurations are listed below). I then download data from Kaggle and upload to AWS S3 bucket. Having those configs ready, I install and import the necessary dependencies (pandas, matplotlib, seaborn) and load the dataset as a pyspark dataframe.

Second, I denormalize the categories that are associated with each business (there may be more than one, presented as a string of comma separated identifiers) and then run some basic analysis on the result.

Third, I join the review ans business datasets to answer the question: are the (written) reviews generally more pessimistic or more optimistic as compared to the overall business rating. 

Fourth, I first join user and review datasets to retrieve the average ratings by the elite users and then join the resultant dataset to business dataset to answer the question: Should the Elite be Trusted? 

## Cluster and Notebook Configs

![cluster](https://github.com/yb19/STA9760-Yelp-Reviews-Project/blob/master/assets/cluster.png?raw=true)
![notebook](https://github.com/yb19/STA9760-Yelp-Reviews-Project/blob/master/assets/notebook.png?raw=true)

## S3 Bucket Management
![s3 bucket](https://github.com/yb19/STA9760-Yelp-Reviews-Project/blob/master/assets/s3%20bucket.png?raw=true)
