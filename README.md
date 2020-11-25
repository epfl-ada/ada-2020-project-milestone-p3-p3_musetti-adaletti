Title: Analysis of retweetability given its sentiment and topic

Abstract:
Users can spread information in Twitter either by crafting new tweets or by using retweet mechanism to re-post the previously created tweets.
We want to know what makes a post retweetable, therefore we will analyze characteristics of a tweet such as its sentiment and its topic.
The sentiment will be extracted via a SOTA sentiment analysis model. Also, sport tweets retweetability will be compared to the one of politics tweets.
The dataset used contains over 1 million tweets.

Research questions:
- **RQ1.** Does the sentiment of the tweets (positive, neutral or negative) have an impact in the retweetability and number of followers?
- **RQ2.** The sentiment of the tweets are somehow related with the day of the weeks (ex Monday vs Friday)?
- **RQ3.** Do other features of the text like the topic (sports or politics) impact on retweetability?

Proposed datasets:
Inflated tweets from EgoTimelines.txt will have the text information, and EgoTimelines.txt contains retweets and further information.

Methods:
- Data collection: We are going to inflate the tweet_ids from EgoTimelines.txt to extract tweets text using [a Twitter API](https://github.com/DocNow/hydrator).
- Sentiment Analysis: We will implement a SOTA Sentiment Analysis model for social media.
- Topic extraction: We will extract tweets of politics and sports with the most popular hashtags of both categories and a list of keywords.

Proposed timeline:
- 1st week: Sentiment and topic extraction
- 2nd week: Correlation between features (sentiment and topic) and retweetability. Ploting figures
- 3rd week: Report and wrap-up
- Deadline: 18th Dec

Organization within the team:

| Team member | Research Question | Task                                                                 |
|-------------|-------------------|----------------------------------------------------------------------|
| Mattia      | RQ1               | Implementing SOTA sentiment analysis model                           |
| Cameron     | RQ1, RQ2          | Analyzing data and correlation of sentiment, time and retweetability |
| Laura       | RQ1, RQ2          | Analyzing data and correlation of sentiment, time and retweetability |
| Marcel      | RQ3               | Extracting tweets by topic (sports/politics), and analyzing them     |

Questions for TAs (optional):

