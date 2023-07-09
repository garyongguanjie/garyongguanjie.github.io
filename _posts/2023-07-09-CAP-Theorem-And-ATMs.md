---
layout: post
title: "Cap theorem and ATMs"
categories:
- Tech
---
![captheorem-image]({{ site.baseurl }}/images/captheorem.jpeg)

# Cap theorem

In this article I will attempt to explain the CAP theorem for distributed systems as simply as possible, using the example of two ATMs. CAP stands for consistency, availability and partition tolerance. According to theory, it is not possible to achieve all 3 at once.

Let's assume that we have two ATMs. ATMs have a few basic functionality such as  deposits, withdrawals and balance enquiries.

For consistency, it implies that each ATM has the exact same data. This means that if a person withdraws the money from one ATM and then checks his balance from both ATMs, it should reflect the same amount.

For availability, it means that the user is able to withdraw the money, or check balances or deposit money, in both ATMs at the same time (assuming the ATMs are functioning).

Partition tolerance can be thought of as the connection between both ATMs. Having 0 tolerance means a perfect connection with no packet drops/losses/delays. In the real world however it is impossible to have 0 partition tolerance because the world is not perfect. One way to solve this is to have 1 ATM, but this is also not feasible because having 1 ATM would result in long queues and also represent a single point of failure where all money would be lost if that single ATM ever fails(and never recovers).

Hence we have to choose between consistency and availability. Why is it possible to not have both at the same time? Let's assume someone withdraws money from ATM 1. Now since partition tolerance is not guaranteed, there is no way for ATM 2 to know the latest balance. Thus ATM 2 has to block all monetary transactions and show a delayed balance enquiry. If we instead sacrifice consistency, it means that both ATMs will show different balances and even allow users to withdraw more than what they actually have - something that should not be allowed for monetary transactions.

When dealing with money you would most often see databases sacrifice availability, though for other types of use cases like, for example storing of tweets, it is okay to be not perfectly consistent. Reconciliation (or some say eventual consistency), can be seen as a method to sacrifice consistency, but do you want to allow people to have negative balances when it is reconciled? Note: A database node can be seen as anything that stores data, whether it's an excel sheet, a piece of paper, a  cache or a relational database or in this simplified case, an ATM machine.
