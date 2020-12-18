Title: How to become a Twitter influencer

Abstract:
The popularity on Twitter it is based on how many people retweet your posts. We want to know what makes a post retweetable and how one can maximize the likelihood of a tweet tobe retweeted, therefore we will analyze characteristics of a tweet such as its sentiment and its topic.
The sentiment will be extracted via a sentiment analysis model. Also, the topic of the tweets and their sentiment will be analysed to understand which is the best combination to get more retweets. The dataset used contains over 1 million tweets.

Research questions:
- **RQ1.** Does the sentiment of the tweets (positive, neutral or negative) have an impact in the retweetability?
- **RQ2.** The sentiment of the tweets are somehow related with the day of the weeks (ex Monday vs Friday) and the time of the day?
- **RQ3.** The retweetability of the tweets are somehow related with the day of the weeks (ex Monday vs Friday) and the time of the day?
- **RQ4.** Do other features of the text like the topic (e.g., sports or politics) impact on retweetability?

Visual Data story:
Beside the read me file, the notebook comes with a visual datastory meant to be seen on a personal computer. It has been tested with the internet browsers Google Chrome and Safari. You can check it out here [How to become a Twitter influencer](https://cameronsmith425.github.io/How-to-become-an-influencer/).

Proposed datasets:
Inflated tweets from EgoTimelines.txt will have the text information, and EgoTimelines.txt contains retweets and further information.

Methods:
- Data collection: We are going to inflate the tweet_ids from EgoTimelines.txt to extract tweets text using [Twitter APIs](https://github.com/DocNow/hydrator). Only tweet IDs associated with English were kept. 
- Data preprocessing: Before using the tweet to perform the sentiment analysis we need to preprocess them. This preprocessing step will be based on two main papers ([Shihab Elbagir and Jing Yang](http://www.iaeng.org/publication/IMECS2019/IMECS2019_pp12-16.pdf) and 
[Toni Pano and Rasha Kashef](https://www.mdpi.com/2504-2289/4/4/33)) and it will incluse noise, stop words and fake tweets (the identificable ones) removal. In addition, for the time analysis, we are going to normalizing the tweets creation day to local time.
- Sentiment Analysis: We will implement a Sentiment Analysis approach based on contextual language models like BERT ([Devlin et al., 2019](https://arxiv.org/abs/1810.04805)) and compare it against rule-based models ([Hutto et al., 2014](http://comp.social.gatech.edu/papers/icwsm14.vader.hutto.pdf)). To make the analysis more robust and be confident that the tweets identified as positive are actually positive and the ones identified as negative are actually negative, we will look for an agreement of the two sentiment analyser. Wi will change the sentiment to neutral every time there is a disagreement between VADER and BERT.
- Topic extraction: We will extract tweets of different topics (sports, politics, music, religion, health, cooking, fashion, family) with the most popular hashtags of both categories and a list of keywords.
- Data visualization: To check if there is a correlation with retweetability for topics and sentiments, several visualizations will be made. These include histogram distributions for various topics and sentiments where number of retweets is on the x axis and number of tweets in on the y-axis. We will also develop graphs in which we visualize if the sentiment of tweets is affected by day of the week: for this each sentiment will have it's own line, and the day of week will be plotted on the x-axis and number of retweets on the y-axis. For this figure it is important that each sentiment dataset is the same size. 
- Data analysis: We will look at regression models to see if there is any correlation between retweeyability and other features such us number of follower and friends, the presence of hashtags and the sentiment of the tweets.

Proposed timeline:
- Week 1: Sentiment and topic extraction
- Week 2: Investigating the correlation between extracted features (sentiment and topic) and retweetability. Plotting figures
- Week 3: Data story
- Deadline: 18th Dec

Organization within the team:

| Team member | Research Question | Task                                                                                                        |
|-------------|-------------------|------------------------------------------------------------------------------------------------------------ |
| Mattia      | RQ1, RQ2, RQ3     | Implementing sentiment analysis model and investigating correlation with other features                     |
| Cameron     | RQ1, RQ2, RQ3     | Data preprocessing. Analyzing data and correlation of sentiment, time and retweetability                    |
| Laura       | RQ1, RQ2, RQ3     | Data preprocessing. Analyzing data and correlation of sentiment, time and retweetability                    |
| Marcel      | RQ4               | Extracting tweets by topic and analyzing them                                                               |

