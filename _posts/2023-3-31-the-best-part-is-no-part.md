---
layout: post
title: The best part is no part
usemathjax: true
categories:
- Tech
---
![100xEngineer]({{ site.baseurl }}/images/bpnp.jpg)

Elon Musk has a saying 'the best part is no part'. When engineering systems be it physical or in software, it is fundamentally important to keep things as simple as possible and eliminate all unnecessary parts. This is because while having more parts may seem 'fanciful', every part has an associated cost.

Let's take the example of building a rocket. Assuming a rocket has 10,000 parts and each part has a reliability of 99.9%. Would you take that rocket? A simple calculation of the overall reliability of the rocket reveals some shocking numbers. Assuming that each part has to work in order for the rocket to function, the overall reliability of the rocket can be calculated as $$0.999^{10000} = 0.00004517$$ or 0.0045%. Clearly a success rate that nobody is willing to accept. Now consider that each part requires someone to build, test and also integrate with the overall rocket, the costs of having too many parts quickly go out of hand and with lower reliability. Now instead imagine if we could build the rocket with only 1000 parts, the reliability quickly goes up to 36%. A massive improvement though it is still preposterous for human flight. (This is in fact what Elon does to make SpaceX 10x cheaper and more reliable than others)

The same can be said for software systems. [Microservices](https://www.youtube.com/watch?v=y8OnoxKotPQ) has been the 'de facto' standard for modern day software architectures. While it does come with its benefits, one should still seek to minimize the number of services as much as possible as each service requires a whole team to build, test and maintain. A 100x engineer does not code 100x faster, in fact he spends 90% of his time thinking what not to write and only 10% of the time writing 1% of what is needed compared to others.

*An engineering philosophy by an inexperienced and naive 0.1x engineer.*
