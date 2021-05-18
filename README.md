> Election Fraud 
---
<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#desctiption">Desctiption</a></li>
        <li><a href="#references">References</a></li>
      </ul>
    </li>
    <li>
      <a href="#Datasets">Datasets</a>
    </li>
    <li><a href="#leave-blank">Twitter JSON Structures</a></li>
    <li><a href="#leave-blank">LEAVE BLANK</a></li>
    <li><a href="#leave-blank">LEAVE BLANK</a></li>
    <li><a href="#leave-blank">LEAVE BLANK</a></li>
    <li><a href="#leave-blank">LEAVE BLANK</a></li>
    <li><a href="#leave-blank">LEAVE BLANK</a></li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About The Project
- [Description](#description)
- [References](#references)


## Datasets
We have three COVID-19 datasets: [**Twitter Firehose**](https://twittercommunity.com/t/new-covid-19-stream-endpoint-available-in-twitter-developer-labs/135540),  [**Synthesio**](https://www.synthesio.com/glossary/social-media-monitoring-platforms/), and [**Emily 1% Public API Dataset**](https://github.com/echen102/COVID-19-TweetIDs).

Here are the timestamps for each datasets. The time frame of each dataset is identical even though the time zones adpoted are different.

* Expected time frame: 
  - Two-weeks for original tweeting:
    - June 15th 00:00 to June 28th 23:59(UTC) 
    - June 14th 19:00 to June 28th 18:59 (CDT)
  - Two-weeks for difussion: 
    - June 29th 00:00 to July 12nd 23:59 (UTC)
    - June 28th 19:00 to July 12nd 18:59 (CDT)
  
We collected data in two phases:

Phase One: 
* Firehose (July 1st 00:00- July 14th 23:59 UTC)
* Public API (July 1st 00:00- July 14th 23:59 UTC)
* Synthesio (July 30th 19:00- July 14th 23:59 CDT)

Phase Two:
* Firehose UTC (June 14th 00:00- June 30th 23:59)
* Public API UTC (June 14th 00:00- June 30th 23:59)
* Synthesio CDT (June 13rd 19:00- June 30th 18:59)

`During summer, Central Daylight Time (CDT) is five hours behind Coordinated Universal Time (UTC)`

We plan to identity all new tweets,posted from June 15th 00:00 to June 28th 23:59(UTC), in the three datasets. For each new tweet, we will allow it diffuses for same duration (i.e., evolution length). In general, the evolution length we decided is **14 days**([Meng et al., 2018](https://www.sciencedirect.com/science/article/pii/S0747563218303613?casa_token=KmXOZwM5HG4AAAAA:JSeYTiMFL1iob8rdkAQ2E6n0VUbRkjOZ0OfAvKgTTF-8pbCvCeOo73J_2RpdQmqhsvx41REVJA)). The transmission cascade of each tweet will be constructed accordingly.


<!-- TWITTER JSON STRUCTURES-->
## Twitter JSON Structures
Basic tweeting types include: (Originally)**Tweeting**, **Reply**, **Retweet**, and **Quote**, while the acutual cases could be more complicated as Twitter users may adopt arbitrary combinations when tweeting, e.g., **retweet other's quote**. The differences reflect in the strcutures of the raw JSONs. 




