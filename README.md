# Semi Supervised Stance Detection
## Problem:
After 2016 US presidential elections detecting political stance of tweet became very important and for this task even though we are having enormous data there is paucity of labels.
## Method:
We are going to use semi-supervised learning method with the guidance of homophily  drawn from rich graph like meta data such as user follower relationship.
## Data Set:
- From US-based users, we collected with a total of 59, 684 tweets from 24, 490 users, with an average of 2.44 tweets and 41.79 followees per user, within the period from 1st January, 2020 to 3rd April, 2020.
- For the Indian counterpart, our crawling period ranges from 26th October, 2019 to 2nd March, 2020, resulting in a total of 176, 619 tweets from 63, 230 users, with an average of 2.79 tweets and 22.93 followees per user.
- Out of these tweets 3, 822 and 4, 185 tweets were annotated from US and India respectively.
- Labels for US-based tweets: Pro-Dem, Anti-Dem, Pro-Rep, Anti-Rep, and, Other.
- Labels for India-based tweets: Pro-BJP, Anti-BJP, Pro-INC, Anti-INC, Pro-AAP, Anti-AAP, and Other.

## Steps to Run:

1. Install the required packages mentioned [here](SANDS/requirements.txt).
2. Download and extract the [data](https://drive.google.com/file/d/1kJuNjSGwT3riZFyMsvm28TBbjYY8neER/view?usp=sharing) and place under the
[working directory](SANDS/)
3. Change directory to SANDS/codes and run 'python3 run_model.py $dataname $splitsize $numclasses' where _$dataname_ can be either INDIA or USA,
_$splitsize_ among 500, 1000, and, 1500. _$numclasses_ currently support 5 and 7 for USA and INDIA arguments, respectively.

## Model Overview:

![image](https://user-images.githubusercontent.com/85636601/203926983-6aaeada7-1fdb-48b0-8491-ea5c260f1bec.png)

## Results:
Data Set | F1 - Score 
| :---: | :---: 
India  | 0.47 
USA  | 0.53 
