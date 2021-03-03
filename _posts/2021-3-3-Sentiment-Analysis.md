---
layout: post
title: 2. How to Analyse Text Sentiment Without the Usage of Neural Networks? 
---

![_config.yml]({{ site.baseurl }}/images/rule_based.png)  

As previously discussed, sentiment analysis algorithms can be conducted in 3 main ways, through a 
 
1. Rule-based approach
2. An autonomous (machine learning) approach
3. A hybrid program that combines both approaches

And although sentiment analysis is an NLP technique, one of the above methods doesn't require the use of machine learning algortithms *at all*! Those [systems of rules](https://www.jair.org/index.php/jair/article/view/10896/25984) are usually handcrafted by humans, so a programmer themselves decides on what "filters" they want for their system. 

But usually, the first step in this process is something known as **tokenization.**

If you've done any programming before and worked with data structures, you are likely familiar with the problem of splitting a string containing sentences into substrings containing only one word. This is exactly what happens during tokenization. Depending on the *delimiter*, the input string will turn into a sequence of *tokens* that are then analyzed separately.

Once the string of data is separated, the program moves on to the clean-up process that consists of the usage of **stopwords**,

 **lemmatization**, 
 
 and **stemming**. 





