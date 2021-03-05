---
layout: post
title: How to Conduct Sentiment Analysis Without Using Neural Networks? 
---

![_config.yml]({{ site.baseurl }}/images/rb.png)

As [previously discussed](https://saidaibrg.github.io/SA-Definition/), [sentiment analysis](https://www.youtube.com/watch?v=O1Xh3H1uEYY) can be conducted in 3 ways: 

1. *Rule-based Approach*
2. [*Autonomous (Machine Learning) Approach*](https://saidaibrg.github.io/ML-Approach/)
3. *A [Hybrid Solution](https://www.researchgate.net/publication/318351105_Hybrid_Tools_and_Techniques_for_Sentiment_Analysis_A_Review) that combines both approaches*  

Surprisingly, one of these methods - a **Rule-based Approach** - doesn't require the use of machine learning algorithms *at all!*  

![_config.yml]({{ site.baseurl }}/images/rb_1.png)
 
Say, we’re given the following text: 

![_config.yml]({{ site.baseurl }}/images/rb_2.png) 

We, as humans, would [logically think](https://www.hilarispublisher.com/open-access/are-neural-networks-imitations-of-mind-jcsb-1000179.pdf) that the emotion of this sentence is POSITIVE. In this tutorial, we’ll try to figure out how to make a computer think so too. 

### First step: Text Pre-Processing.

Before trying to [make a computer](https://www.digitalocean.com/community/tutorials/how-to-perform-sentiment-analysis-in-python-3-using-the-natural-language-toolkit-nltk) understand word definitions, we need to make the input data more understandable with the help of the following [procedures](https://dair.ai/notebooks/nlp/2020/03/19/nlp_basics_tokenization_segmentation.html): 

* **Tokenization**

If you've done any programming before and worked with data structures, you are likely familiar with the problem of splitting a string of text into substrings consisting of one word. This is exactly what happens during [*tokenization*](https://medium.com/@jeevanchavan143/nlp-tokenization-stemming-lemmatization-bag-of-words-tf-idf-pos-7650f83c60be). Depending on the *delimiter* (whether it’s a space, comma, “but”), the input string will turn into a sequence of *tokens* or separate units of text.
* **Noise Removal aka “Clean-Up”**

This [process](https://www.kdnuggets.com/2019/04/text-preprocessing-nlp-machine-learning.html#:~:text=Noise%20removal%20is%20about%20removing,is%20also%20highly%20domain%20dependent.) removes all URLs, hashtags, extra letters, whitespaces from the text.
* **Stemming**

This step basically “cuts off” the ending of the word to bring it back to its standard state. For example, “working” becomes “work” and “flowers” becomes “flower.” 
* **Lemmatization**

You might think that stemming isn’t [accurate](https://www.toptal.com/deep-learning/4-sentiment-analysis-accuracy-traps) enough, as it doesn’t acknowledge whether the word is a verb or a noun. [Lemmatization](https://towardsdatascience.com/text-preprocessing-with-nltk-9de5de891658) is a more complex function that takes into account the lexical meaning of the word before converting the word to its standard state.  

The result is going to look somewhat like this: 

![_config.yml]({{ site.baseurl }}/images/rb_3.png)  

### Second step: Dictionary “Look-up.”

Once the input is [concise and understandable](https://www.kdnuggets.com/2019/04/text-preprocessing-nlp-machine-learning.html#:~:text=Noise%20removal%20is%20about%20removing,is%20also%20highly%20domain%20dependent.), the program moves on to the lexical analysis of the text. This happens with the assistance for [**lexicons**](https://www.mitpressjournals.org/doi/pdf/10.1162/COLI_a_00049): databases, which act very similarly to dictionaries. However, instead of displaying a definition for each word, they return their **polarity**: a number that measures their “positiveness.” Since there’s a [big variety of dictionaries](https://www.tidytextmining.com/sentiment.html#sentiment) out there, so the scale for polarity varies for each of them.

![Alt Text](https://media.giphy.com/media/L8ETAZEmZ8VtY1ed6D/giphy.gif)

### Third step: Summation and Results.
But generally, in the [rule-based method](https://monkeylearn.com/sentiment-analysis/), the sentiment of the whole text block is considered to be the sum of the polarity assigned to each word or token.  

## #GoodNewsYay 
Thankfully, there are ways to automate this process! Tools like [Vader](https://t-redactyl.io/blog/2017/04/using-vader-to-handle-sentiment-analysis-with-social-media-text.html), [WordNet](https://pythonprogramming.net/wordnet-nltk-tutorial/), [SentiWordnet](https://www.coursera.org/lecture/text-mining-analytics/5-6-how-to-do-sentiment-analysis-with-sentiwordnet-5RwtX) make sentiment analysis easy and versatile. What’s more, there’re many [lexicons](https://www.kdnuggets.com/2018/08/emotion-sentiment-analysis-practitioners-guide-nlp-5.html) with varying functions and scales for polarities that can be chose over each other for specific purposes of your project.  



