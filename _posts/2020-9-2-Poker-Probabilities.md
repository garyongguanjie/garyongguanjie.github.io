---
layout: post
title: Exploring Poker Probabilities
--- 
![poker-television]({{ site.baseurl }}/images/pokerImages/poker-television.jpg)

Recently after graduation, I had some time to play Zynga poker. Zynga Poker uses fake money and is not similar to real life poker. However this has pique my interest on how to play poker optimally. This posts aims to calculate the probabilites from the perspective all the player.

Calculating poker winning probabilities is not easy. The probabilites that one sees on televised poker tournaments often involves enumerating all possible outcomes. This is often computationally expensive and requires highly optimized code. It is also important to note that the probabilites in these televised competitions calculates the probabilies given that **all player cards are known**.

For example in the image above the probabilities are calculated with 8❤ and 9♦ for the 1st player and 2♣ and K♣ for the 2nd player. Hence in the above image the probability that player 1 wins is computed as 
```
P(player1 wins | player1 has 8❤ and 9♦ and player 2 has 2♣ and K♣)
```
However if we are player 1 we wont have information about player 2.
Hence what we would want is 
```
P(player1 wins | player1 has 8❤ and 9♦)
```

Unfortunately there are not many programs that calculate the above probability. 

# Estimating Probabilities for 5 player Texas Holdem
Due to the high computational costs I have decided to estimate them. Estimation is a simple tasks. We just need to randomly shuffle and simulate the playouts and count the number of times that we win. For the purpose of this post I have decided to investigate 5 player Texas Holdem Poker from the perspective of a single player.

# Preflop Probabilites

Here are the estimated probabilites for unsuited preflop and suited preflop. For those unfamiliar preflop is where there is no card shown yet.

[unsuited-preflop]({{ site.baseurl }}/images/pokerImages/unsuited-preflop.PNG)

[suited-preflop]({{ site.baseurl }}/images/pokerImages/suited-preflop.PNG)

As one would expect suited probabilites are much higher than unsuited. It gives about a 6% advantage. As a general rule one shoulld almost always fold if your winning probabilites is less than 1/number of players. Also note that pair starting hands are very much higher than the average hand and one should almost always play if one has 8 pair or higher.

# Postflop Probabilites

Post Flop is harder to investigate as there are so many possibilites and it is impossible to put all of them in a table. For the purpose of this let us investigate the winning probabilities if you have 7,8.

### Post flop Single Pair

| Hand | Board | Winning Probabilites |
| --- | --- | --- |
| 7 ❤ 8 ♠ | 8 ♣ 5 ❤ J ♣ | 0.279 |
| 7 ❤ 8 ♠ | 8 ♣ 5 ❤ 2 ♣ | 0.269 |
| 7 ❤ 8 ♠ | 8 ♣ 5 ❤ A ♣ | 0.258 |

### Post flop two pair

| Hand | Board | Winning Probabilites |
| --- | --- | --- |
| 7 ❤ 8 ♠ | 8 ♣ 7 ♦ A ♣ | 0.536 |
| 7 ❤ 8 ♠ | 8 ♣ 7 ♦ 2 ♣ | 0.567 |

### Post flop almost a straight

| Hand | Board | Winning Probabilites |
| --- | --- | --- |
| 7 ❤ 8 ♠ | 5 ♣ 9 ♦ 2 ♣ | 0.186 |
| 7 ❤ 8 ♠ | 6 ♣ 9 ♦ 2 ♣ | 0.306 |
| 7 ❤ 8 ♠ | 6 ♣ 9 ♦ A ♣ | 0.297 |

### Post flop straight

| Hand | Board | Winning Probabilites |
| --- | --- | --- |
| 7 ❤ 8 ♠ | 6 ♣ 9 ♦ T ♣ | 0.775 |

### Post flop almost a flush

| Hand | Board | Winning Probabilites |
| --- | --- | --- |
| 7 ❤ 8 ❤ | 2 ❤ Q ❤  A ♦ | 0.325 |
| 7 ♦ 8 ❤ | 2 ❤ Q ❤  A ❤ | 0.188 |

### Post flop almost a straight flush

| Hand | Board | Winning Probabilites |
| --- | --- | --- |
| 7 ❤ 8 ❤ | 6 ❤ 9 ❤ A ♣ | 0.499 |

### Post flop flush

| Hand | Board | Winning Probabilites |
| --- | --- | --- |
| 7 ❤ 8 ❤ | 2 ❤ 3 ❤ Q ❤ | 0.679 |

### Post flop straight flush

| Hand | Board | Winning Probabilites |
| --- | --- | --- |
| 7 ❤ 8 ❤ | 6 ❤ 9 ❤ T ❤ | 1.0 |

So two pair is better than having almost a flush/straight. Hence if you suspect your opponent has a two pair and you should not hope for a straight/flush.

# Conclusion

Of course the art to poker is more than just knowing the probabilites. Note that the above probabilites do not take into account actions taken by your opponents! If an opponent raises he is more likely to have good cards decreasing your winning chances. Or your opponent might be bluffing. Note that the objective of poker is not to win the most number of hands but to win the most amount of money. Hence to be a good poker player one needs to convince your opponent that you are bluffing when you are not and bluff when your opponent thinks you are telling the truth while minimizing the loss if caught bluffing. As a last note, AI has already reached [superhuman level](https://ai.facebook.com/blog/pluribus-first-ai-to-beat-pros-in-6-player-poker/) with poker.