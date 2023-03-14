---
layout: post
title: Stop discrimminating Bachelors in ML!
image: images/bachelor_disc/bachelor_disc.jpg
categories:
- Data Science
---

![pic]({{ site.baseurl }}/images/bachelor_disc/bachelor_disc.jpg)

So you have just completed your bachelor's degree. You have taken some electives in machine learning and in your free time you took Andrew Ng's Machine Learning course as well as Stanford's CS231n Computer Vision Course. You are all ready to be a Data Scientist/ML engineer until you see the job post with the following description *Minimum 3 years of experience with a Phd or 7 years of experience with a Msc*. You become demoralized and look for other jobs only to find that most jobs *strongly prefer* a postgraduate degree. This article aims to answer 2 questions should you take up a postgraduate degree and should employers really be looking for people with postgraduate degrees.

## Should you take up a postgraduate degree?

To answer the question you must first understand what job do you really want. In general ML related jobs can be broken down into 4 categories.

1. Data Analyst
    - In this role your task is to analyze the data using statistical means and provide business insights to guide the product in the right direction. 
    This role requires good knowledge of statistics and SQL as well as some data visualization tools. You should also be able to communicate your insights via tableau or powerpoints or whatever means necessary. You may be required to do A/B testing of new product features and analyze the results.

2. Data Scientist
    - Unfortunately this term is often used together with data analyst to mean the same thing. Do read the job description to know what you are getting into. For the purpose of this article, Data Scientist refers to roles that requires one to analyze the data and do some sort of modelling in order to predict something. You may be required to do AB testing of your models and see if it indeed improves the product/revenue.

3. Machine Learning Engineer
    - This role is somewhat similar to the data scientist role. However your role is closer towards the engineering side of things.Your task would be to build and deploy models with the assistance of data scientist.

4. Research Scientist
    - This role is the least common of all. In this role you are required to do research to solve novel problems which cannot be solved by any plug and play model that is easily found online. Sometimes you are required to publish papers.

In terms of *data science* technical skills requirement `Data Analyst < Machine Learning Engineer < Data Scienitst < Research Scientist`. While machine learning engineers have technically hard tasks as well their tasks are in general closer to software engineering.

Now to answer the question do you need a postgraduate degree? And the answer is it depends. If you have 0 CS/Math background you almost definitely need a masters for any of the roles. However if you already have a relevant bachelors, you do not need one for analyst related roles. But for data scientist and machine learning engineers, you are *strongly preferred* to require one. For research engineers you almost always require a Phd. 

Here are some statistical results to back up my [claim](https://www.kaggle.com/garyongguanjie/should-i-pursue-higher-education). Also annecdotal evidence (random sample across companies of varying sizes) from linkedin premium suggests that around 40% of Data science and MLE job *applicants* possess at least a masters degree (even for smaller companies and startups!). For reference for SWE roles I have observed less than 10% of applicants possess at least a master's degree. Note that there are always exceptions such as [Chris Colah](https://colah.github.io/about.html) who is a research engineer at google despite not even having a bachelor's degree. However it is my belief that you have to be exceptional in order to be an exception to the rule.

Lastly in an ideal world I would say 'You should take up a postgraduate degree to learn, not to get a job'. However note that a master's/Phd degree requires alot of commitment which often require several thousand dollars and at least 1.5 years of your time. This is something that not many can commit to, even if your purpose is to learn and get a job. In many cases many universities copy their course content from openly available popular courses from top universities. In addition the ML field is blessed with people publishing free books and research papers which allows one to learn it for absolutely free.

There is of course some ways to circumvent this requirement.

1. Win a kaggle competition
    - Winning is hard. Perhaps even harder than getting a job at google. You might not even have the necessary compute requirements to win. Also HR likely has no clue what kaggle is so you never get interviewed.

2. Work at a big tech company to prove your worth
    - Often recruiter's would look at your resume and see your work experience first, specifically your previous company and job title. This however presents a chicken and egg problem where you cant get a job without first having a big tech company (with a relevant job) on your resume.

3. Leverage your connections
    - Show off your (excellent) work (projects/youtube/blog/kaggle whatever it takes)
    - Make friends and go to ML related social events
    - Somehow get a referral to a top tech company

## Should employers require a postgraduate degree?

This answer is trickier. Ideally it would be great to evaluate each candidate solely based on their machine learning skills (disregarding their education levels), however human resources are finite and it is not possible to evaluate every candidate. While I would not say that the skill levels of Bsc < Msc < Phd for every candidate, on the average case this is true. So what eventually happens is that they only interview candidates who possess a masters degree and above. 

The next question is of course, why does this bias only exist in the field of ML? I believe the reason is that ML is a highly scientific practice which requires alot of knowledge.

For example I believe that the prerequisite **fundamentals** to be good at ML are

1. CS
    - Coding fundamentals
    - Data Structures and algorithms

2. Math
    - Mastery of algebra
    - Probability
    - Statistics
    - Linear Algebra
    - Single variable calculus
    - Multivariable (Matrix/Vector) Calculus
    - Information theory

And the key here is that these are just the *prerequisites*. For most people other than the most motivated / highest aptitude, learning these prerequisites (at sufficient depth) alone would take at least 1 year if not more. Alot of people tend to be weak in *at least one* of these fundamentals. I have found my self to be weak(er) at linear algebra as well as multivariable calculus. 

Many of these prerequsite topics are covered in the first 2-3 years of undergraduate courses. And since not everyone wants to do ML, most universities have to cover other more generic courses leaving very little time for the teaching of the actual ML courses. As a result employers notice this and only hire people with postgraduate degrees where they actually go in depth into ML.

Now I dont have a postgraduate degree and hence need to justify why employers should not require one (or discrimminate against not having one). 

1. Abstraction of ML doesnt require in depth knowledge
    - Unless you are a research engineer, chances are you wouldnt need to code out the actual ML algorithm. But rather you would use one that is already available. As a result most people do not actually need to know how the algorithm works and only need to know what the algorithm does. (Can anyone name 5 hyperparemeters of xgboost?) Hence alot of the time is spent doing data wrangling, and exploring what the input/output space of the models should be rather than the on the actual model itself.
2. Fundamentals are underrated
    - It is my personal belief that all you need is **one** ML course + strong fundamentals and you would be better than 99% of the people out there. What I have found is that in general most people (including myself) tend to focus too much on the *state of the art* methods but have yet to master the fundamentals.
    -  It is important to note that many of these *fundamentals* are taught at an undergraduate level. And also alot of these *fundamentals* are **not** taught at the postgraduate level. Hence it is not necessarily the case that a masters/phd is better than a bachelors especially for those who did not do CS/Math during their undergraduate days. For some evidence see this [link](https://blog.alinelerner.com/how-different-is-a-b-s-in-computer-science-from-a-m-s-in-computer-science-when-it-comes-to-recruiting/) where the author has found that bachelor candidates are actually better than masters when it comes to fundamentals.
    - As an example how many people would be able to discover such a [pitfall](https://towardsdatascience.com/pitfalls-with-dropout-and-batchnorm-in-regression-problems-39e02ce08e4d) if they faced the same problem. The key here is to discover that something is wrong in the first place and then figuring out why. The author clearly has very good fundamentals and I would personally hire him even if he has no clue about transformers or graph neural networks.
3. ML in real life is closer to SWE
    - [ML is alchemy?](https://www.science.org/content/article/ai-researchers-allege-machine-learning-alchemy#:~:text=Speaking%20at%20an%20AI%20conference,one%20AI%20architecture%20over%20another.) Is doing randomized grid search ML or SWE? What about trying different models and see what works and what doesnt? A lot of ML actually requires trial and error, and the ability to write your code such that it is flexible and adaptable to different models/trials/data is SWE not ML.

## Conclusion
Thanks for reading my article. And if you are in charge of hiring ML candidates, I hope to have changed your perception. Lastly, this article possesses a high personal bias and might change if I pursue higher education.
