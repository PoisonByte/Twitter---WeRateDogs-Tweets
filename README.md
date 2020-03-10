# Twitter---WeRateDogs-Tweets
Data Analysis of Twitter information for #WeRateDogs

During my data analyst, wrangling for the Wrangle_Act Project it was easier first working with the importing the twitter-archive-enhanced.csv. Since this is the most common file we’ve worked with at Udacity. After reading the dataframe I began to run some analysis on the data. Already taking into account some cleaning processes that will be needed with each dog stage being separate and containing such high values for none. Noticing for the name column that there were 745 values for none and started to see oddly placed names in the data.I did see that there was a few values in the tweet id possibly due to some of the retweeted data. Finally the observation I notice was in the text values some of the scores were off and this needed to be corrected. 
Next I began to import the image_predictions.tsv. Once I imported the images from the tsv file I wrote the to a csv file. Which supplied more helpful info for dog breeds, images and even more tweet_id’s. I beginning to see the connection for each dataframe might be linked to the tweet_id column. After exploring some of the data I began to think of some insights the conclusion might bring to the report. To test the images were valid I went through just about all of them and displayed a few through our my report. I did find I had to switch my code up for the wrangle_act vs the act_report to display these images. 
The code I used for wrangle act was: 
	from IPython.display import display 
Image(url = 'https://pbs.twimg.com/media/CcLq7ipW4AArSGZ.jpg')

The code I used for the act_report:
	from IPython.display import display, Image
Image(url = 'https://pbs.twimg.com/media/CZhn-QAWwAASQan.jpg')

I found a helpful resource on stack overflow that assisted me in this process. I then obtained my credentials from Twitter to down load the remaining info for the tweet-json file. However, after receiving my keys and attempting to code the process was very lengthy in time and once it finished all the data never fully stored. I searched and actually found an answer in the Udacity chat that helped supplied me with the info use the tweet-json.txt that was already provided to us, and was successful in writing this into a new csv file.
	Now it that the process of importing all three dataframes was complete I began to define the which processes needed to be cleaned. 
1.	Update Timestamp column to datetime format
2.	Update tweet_id from integer to string
3.	Remove columns in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp
4.	Update P1_conf, P2_conf, and P3_conf t string
5.	Update ratings to correct decimals
6.	Create and overall rating
7.	Correcting doggo, floofer, pupper and puppo to one column dog_stage
8.	Merge dataframes
9.	Clean Source data
10.	Fix lowercase names and decrease 'none'
Then after cleaning how this would apply to the tidiness of the report 
1.	Create one column for dog stage
2.	Merge all dataframes

As per our education I made clean copies of each dataframe before making any adjustments. Then one by one I was coding and testing each one of my ten defined processes. Most of the knowledge came from notes in this section but I found most support from overstack. The areas I found trouble with was fixing the names where my code gave me an typeerror but I found if I continued with the code itself the result was successful. After about all my cleaning I waited to lastly to merge each dataframe into one which gave me the most trouble. I found the articles discussing left and right joins but I decided upon an otter was best for me. After successfully merging my data I noticed a few more changes needed before finally saving all into a master csv and finishing with some data analysis!
