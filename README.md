# as_t
 ## What need to be done:
EC shop manages facebook adverting and yahoo adverting and insight.json has ads’ insights data for December 2020.
Create a program that shows the blow calculations on console by using the json data.

 1. The sum of each field (impressions, sales, conversions, clicks, spend) for each provider, here they are Facebook and Yahoo
 2. Calculate CPC, CPA, CTR, CVR, ROAS (explained below) from the sum of Facebook and Yahoo and show them on console 

 ## How to parse json
 ```php
 $json = file_get_contents('insight.json');
 $json = mb_convert_encoding($json, 'UTF8');
 $data = json_decode($json, true);
 ```
 ## Fields:
 |field|meaning|
 |:--:|:--:|
 |impressions|the number of times that an ad is viewed|
 |sales|sales from ads|
 |conversions|an action that's counted when someone interacts with your ad (such as registration and  purchase)|
 |clicks|how many times ads are clicked|
 |spend|how much ads spent|
 |provider|ad provider (such as Facebook, Yahoo, etc)|

 ## Terminologies:
 |teminology|meaning|how to calculate|
 |:--:|:--:|:--:|
 |CPC|cost per click|spend / clicks|
 |CPA|cost per acquisition|spend / conversions|
 |CTR|Click through rate is the number of clicks divided by the total number of impressions.|clicks / impressions * 100 (%)|
 |CVR|conversion rate, in in-app advertising is the percentage of users who saw an app-install ad, clicked on it, and converted through some pre-specified action.|conversions / clicks * 100 (%)|
 |ROAS|return on advertising spend is the amount of revenue your business earns for how much it spends on advertising |sales / spend * 100 (%)|
