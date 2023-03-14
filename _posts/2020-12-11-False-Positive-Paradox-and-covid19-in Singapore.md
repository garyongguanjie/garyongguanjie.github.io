---
layout: post
title: False Positive Paradox and Covid19 in Singapore
categories:
- Data Science
---

Singapore is one of the few nations in the world with very low daily infections of covid19. The recent case of a false positve on a
cruise ship has sparked a discussion of false positives in PCR tests on covid 19. It is important to take note of false positives with more aggressive testing on people with no symptoms or connections to prior cases.

# What is the False positive paradox?
False positive paradox or [base rate fallacy](https://en.wikipedia.org/wiki/Base_rate_fallacy) is the phenomena where there are more false positive results than true positives. This is seemingly counter intuitive as someone with positive result on covid19 is more likely not to have the disease. This is especially the case in Singapore as the base rate for covid19 infections in very low.

# Singapore case study

Let's examine this phenomena in Singapore. The base rate of daily infection in Singapore is fairly low. There are about 10 cases of covid19 cases in Singapore. Assuming this numbers are correct, the base rate in Singapore is around 10 divided by [number of swabs per day ~25 000 = 0.0004](https://www.todayonline.com/singapore/explainer-how-often-are-false-positive-covid-19-test-results-and-why-do-they-happen). The accuracy of a [PCR covid19 test is around 0.998](https://www.todayonline.com/singapore/explainer-how-often-are-false-positive-covid-19-test-results-and-why-do-they-happen). The probability that we are interested in is `p(covid19 | + test)` which is the probability that someone has contracted covid19 if they have tested positive.

To solve this number we need to use [bayes theorem](https://en.wikipedia.org/wiki/Bayes%27_theorem).

```
p(covid19 | +test) = p(+test|covid19)*p(covid19)/p(+test)

Calculating p(+test)
p(+test) = p(+test|covid19)*p(covid19) + p(+test|no covid19)*p(no covid19) 
         = 0.998*0.0004 + (1-0.998)*(1-0.0004)
         = 0.0023984

p(covid19 | +test) = 0.998*0.0004/0.0023984
                   = 0.16644429619
```

Thus the probability of contracting covid19 if you are tested positive is around 16%. This low number is also the reason why Singapore conducts at least two tests for every suspected case. However it is important to note that this number will only go down with more aggressive testing as the above tests are only on **suspected** cases. In the future many public events might require massive testing even if they are **not suspected** to have covid19 and this would result in a number even lower than 16%. Unfortunately for the case of covid19, it is actually okay to have some false positives as the worse case for people with false positives are that they are simnply quarantined. What we should be more worried about are false negative cases where even 1 case is 1 too many. Hence if there are two tests taken for a single person even if one of the tests turns out positive we should quarantine them.