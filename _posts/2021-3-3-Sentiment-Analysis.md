---
layout: post
title: How to Analyse Text Sentiment Without the Usage of Neural Networks? 
---

![_config.yml]({{ site.baseurl }}/images/rule_based.png)  

As previously discussed (link), sentiment analysis can be conducted in 3 ways: 

1. Rule-based Approach
2. Autonomous (Machine Learning) Approach
3. A Hybrid Solution that combines both approaches 

Surprisingly, one of these methods - **Rule-based Approach** - doesn't require the use of machine learning algorithms *at all*!  

# Theory Behind the Rule-Based Method for Sentiment Analysis: 

![_config.yml]({{ site.baseurl }}/images/rb_1.png) 

Say, we’re given the following text: 
![_config.yml]({{ site.baseurl }}/images/rb_2.png) 

We, as humans, would logically think that the emotion of this sentence is POSITIVE. In this tutorial, we’ll try to figure out how to make a computer think so too. 

### 1st step: Text Pre-Processing

Before trying to make a computer understand word definitions, we need to make the input data more understandable with the help of the following procedures: 

* **Tokenization**
If you've done any programming before and worked with data structures, you are likely familiar with the problem of splitting a string of text into substrings consisting of one word. This is exactly what happens during *tokenization*. Depending on the *delimiter* (whether it’s a space, comma, “but”), the input string will turn into a sequence of *tokens* or separate units of text.
* **Noise Removal aka “Clean-Up”**
This process removes all URLs, hashtags, extra letters, whitespaces from the text.  
* **Stemming**
This step basically “cuts off” the ending of the word to bring it back to its standard state. For example, “working” becomes “work” and “flowers” becomes “flower.” 
* **Lemmatization**
You might think that stemming isn’t accurate enough, as it doesn’t acknowledge whether the word is a verb or a noun. Lemmatization is a more complex function that takes into account the lexical meaning of the word before converting the word to its standard state.  

The result is going to look somewhat like this: 
![_config.yml]({{ site.baseurl }}/images/rb_3.png)  

## 2nd step: Dictionary “Look-up”

Once the input is concise and understandable, the program moves on to the lexical analysis of the text. This happens with the assistance for **lexicons**: databases, which act very similarly to dictionaries. However, instead of displaying a definition for each word, they return their **polarity**: a number that measures their “positiveness.” Since there’s a big variety of dictionaries out there, so the scale for polarity varies for each of them.

(gif)

## 3rd step: Summation and Results
But generally, in the rule-based method, the sentiment of the whole text block is considered to be the sum of the polarity assigned to each word or (token).  

## #GoodNews 
Thankfully, there are ways to automate this process! Tools like Vader, WordNet, SentiWordnet make sentiment analysis easy and versatile. What’s more, there’re many lexicons with varying functions and scales for polarities that can be better over each other for specific projects.  



