Title: Analysis of retweetability given its sentiment and topic

Abstract:
Users can spread information in Twitter either by crafting new tweets or by using retweet mechanism to re-post the previously created tweets.
We want to know what makes a post retweetable, therefore we will analyze characteristics of a tweet such as its sentiment and its topic.
The sentiment will be extracted via a SOTA sentiment analysis model. Also, sport tweets retweetability will be compared to the one of politics tweets.
The dataset used contains over 1 million tweets.

Research questions:
- **RQ1.** Does the sentiment of the tweets (positive, neutral or negative) have an impact in the retweetability and number of followers?
- **RQ2.** The sentiment of the tweets are somehow related with the day of the weeks (ex Monday vs Friday)?
- **RQ3.** Do other features of the text like the topic (e.g., sports or politics) impact on retweetability?

Proposed datasets:
Inflated tweets from EgoTimelines.txt will have the text information, and EgoTimelines.txt contains retweets and further information.

Methods:
- Data collection: We are going to inflate the tweet_ids from EgoTimelines.txt to extract tweets text using [Twitter APIs](https://github.com/DocNow/hydrator).
- Sentiment Analysis: We will implement a Sentiment Analysis model based on contextual language models like BERT ([Devlin et al., 2019](https://arxiv.org/abs/1810.04805)) and compare it against rule-based models ([Hutto et al., 2014](http://comp.social.gatech.edu/papers/icwsm14.vader.hutto.pdf))
- Topic extraction: We will extract tweets of politics and sports with the most popular hashtags of both categories and a list of keywords.

Proposed timeline:
- Week 1: Sentiment and topic extraction
- Week 2: Investigating the correlation between extracted features (sentiment and topic) and retweetability. Ploting figures
- Week 3: Report and wrap-up
- Deadline: 18th Dec

Organization within the team:

| Team member | Research Question | Task                                                                                    |
|-------------|-------------------|-----------------------------------------------------------------------------------------|
| Mattia      | RQ1, RQ2          | Implementing sentiment analysis model and investigating correlation with other features |
| Cameron     | RQ1, RQ2          | Analyzing data and correlation of sentiment, time and retweetability                    |
| Laura       | RQ1, RQ2          | Analyzing data and correlation of sentiment, time and retweetability                    |
| Marcel      | RQ3               | Extracting tweets by topic (sports/politics), and analyzing them                        |

Questions for TAs (optional):

