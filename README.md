# Twitter_Data_Extract
Extraction of Twitter data based on filter option using library Tweepy to hit Twitter data extraction API

The Twitter_Extract file contains complete code for extracting tweets in timely manner, for a long period of time.

A Sample of Twitter data extracted is also uploaded in the directory.

It is mainly related to api.search method of Twitter API to filter tweets based on its content.

by Default a filter mentioned in the code is to avoid retweets.

In the same variable you can specify other filter options with a space between multiple filter options.

tweets_df function collects required data from a single tweet's json document.
If other data is required from the json document apart from the ones mentioned, a sample is provided below.

{
  "created_at": "Thu Apr 06 15:24:15 +0000 2017",
  "id_str": "850006245121695744",
  "text": "1\/ Today we\u2019re sharing our vision for the future of the Twitter API platform!\nhttps:\/\/t.co\/XweGngmxlP",
  "user": {
    "id": 2244994945,
    "name": "Twitter Dev",
    "screen_name": "TwitterDev",
    "location": "Internet",
    "url": "https:\/\/dev.twitter.com\/",
    "description": "Your official source for Twitter Platform news, updates & events. Need technical help? Visit https:\/\/twittercommunity.com\/ \u2328\ufe0f #TapIntoTwitter"
  },
  "place": {   
  },
  "entities": {
    "hashtags": [      
    ],
    "urls": [
      {
        "url": "https:\/\/t.co\/XweGngmxlP",
        "unwound": {
          "url": "https:\/\/cards.twitter.com\/cards\/18ce53wgo4h\/3xo1c",
          "title": "Building the Future of the Twitter API Platform"
        }
      }
    ],
    "user_mentions": [     
    ]
  }
}

This is not the complete dictionary for the twitter json document, just a sample.

If you require anything specifc and you dont find it above, you can look for it here: https://developer.twitter.com/en/docs/twitter-api/v1/data-dictionary/overview/intro-to-tweet-json

The data is organized, duplicate tweets are removed and then saved as an .CSV file.

The file is saved in the same directory and the file can be re-run multiple times to collect data day to day for a long period of time without having to change any part of the code.
