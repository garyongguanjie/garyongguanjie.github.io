---
layout: post
title: Why do some players fail to perform in the English Premier League?
categories:
- Data Science
---
![pic]({{ site.baseurl }}/images/football_analysis/Arsenal-Man-Utd-Chelsea.jpg)

100 goals 50 assists. A fantastic statistic. Millions dropped to bring player to the Premier League. Time and again we have seen poor performances despite having seemingly good performances in previous seasons. Are these poor performances simply a result of their failure of adapting to a different culture or system? Or is it simply due to their lack of competence?

To be fair there are multiple reasons why a player cannot perform as well. Perhaps they are not able to adapt socially or may be they have an inferiority complex. The coach may also play them in the wrong position. However there are certain scenarios which exposes their lack of competence which were previously hidden due toa multitude of reasons. Some of these reasons include: Playing in a much stronger team, playing against much weaker opponents, playing with an extremely skilled partner who covers your weakness/causes confusion amongst opponents. Because of these reasons it is very hard to objectively judge a true skill of a player. This results in many incorrect judgements which can be very costly. A simple yet objective way to evaluate player statistics is to judge their performance with respect to the difficulty of the league. There is often a debate on which league is indeed the best.

For starters let's analyse some simple champions league statistics.

| league                   |   winner | runners up | enter finals |
|:-------------------------|---------:|-----------:|-------------:|
| English Premier League   |  14      | 10         | 24           |
| Spanish La Liga          |  18      | 11         | 29           |
| German Bundesliga        |  8       | 10         | 18           |
| Italy Serie A            |  12      | 16         | 28           |
| French Ligue 1           |  1       | 6          | 7            |

We see that the spanish teams have won the champions league the most number of times, while French teams have only won once.
Observing champions league wins gives us a rough idea on which league is the strongest. However it is important to note that only two teams in the spanish league have won the champions league, indicating that it is mainly dominated by these two clubs. What we really want is to evaluate the strength of the average club within each league. Unfortunately there is no such competition for the battle of averages. Thankfully for us the people at [fivethirtyeight](https://projects.fivethirtyeight.com/soccer-predictions/global-club-rankings/) have made pretty complex analysis through mathematical modelling to estimate the strength of each team. 

To better understand how they formulate these rankings you may take a look here [https://fivethirtyeight.com/methodology/how-our-club-soccer-predictions-work/]([https://fivethirtyeight.com/methodology/how-our-club-soccer-predictions-work/]). Here is a short summary of the terms that they used.

Terms
* Rank - Rank of the club (lower is better)
* off - Offensive score of club (Expected no. of goals against average team) (higher is better)
* def - defensive score of club (Expected no. of goals conceded against average team)(lower is better)
* spi - Soccer Power Index - proprietary score by fivethirtyeight (higher is better)

Here are the graphs plotting the distributions.

Rank

![rank]({{ site.baseurl }}/images/football_analysis/rank.png)

Spi

![spi]({{ site.baseurl }}/images/football_analysis/spi.png)

Mean Scores

| league                 |     rank |     off |      def |     spi |
|:-----------------------|---------:|--------:|---------:|--------:|
| English Premier League |  42.7    | 2.0175  | 0.73     | 73.2745 |
| Spanish La Liga        |  55.45   | 1.869   | 0.771    | 70.0275 |
| German Bundesliga      |  58.6667 | 2.02778 | 0.898333 | 69.4594 |
| Italy Serie A          |  85.8    | 1.839   | 0.9875   | 64.3585 |
| French Ligue 1         | 106.1    | 1.6455  | 1.0045   | 60.2    |

Median Scores

| league                 |   rank |   off |   def |    spi |
|:-----------------------|-------:|------:|------:|-------:|
| English Premier League |   32   | 1.97  | 0.755 | 73.935 |
| Spanish La Liga        |   50.5 | 1.755 | 0.835 | 69.075 |
| German Bundesliga      |   53.5 | 1.95  | 0.97  | 68.515 |
| Italy Serie A          |   89.5 | 1.695 | 1.01  | 61.3   |
| French Ligue 1         |  116.5 | 1.57  | 1.01  | 57.685 |

Based on the ranks we can observe that the English Premier League is the strongest league. This is not surprising as the EPL has the most money in the world and the most talented players would always be attracted there. The median French club is rank 116th while the median English club is rank 32nd! Now that we know the relative strength of the leagues we are able to better understand why some players are not able to perform up to expectations. Clubs should always beware that they should not overpay for a player with an awesome statistic especially if they play in one of the weaker leagues.