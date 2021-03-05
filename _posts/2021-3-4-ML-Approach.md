---
layout: post
title: Simple Guide to using Machine Learning in Sentiment Analysis Applications 
---

![_config.yml]({{ site.baseurl }}/images/ml.png)


While a rule-based approach to sentiment analysis is straightforward and quick, in most cases, it lacks accuracy. Therefore,  although it’s useful sometimes to know the degree of “positiveness” / “negativeness” of each word, knowing the **context around a word** is more important. 

Take a look at these tweets: 
![_config.yml]({{ site.baseurl }}/images/tweet1.png)

![_config.yml]({{ site.baseurl }}/images/tweet2.png)

You, as a human reader, can clearly see that these tweets, despite the words “bomb” and “murderer,” do NOT have any NEGATIVE sentiment. That happens because your amazing brain is able to understand the given text *with* its context and make right conclusions about it. Easy-peasy, right?

Turns out this is not that of a simple task for computers, so machine learning and neural networks come handy to do it.

![_config.yml]({{ site.baseurl }}/images/ml_1.png)

### The biggest difference between a rule-based and ML-based approaches is the role of the **context** for each word. In the ML-based sentiment analysis, the polarity of every word is determined by taking into account the polarity and lexical meaning of the neighboring words of this token, whereas in a rule-based method only a polarity of a specific word is calculated.  

To understand the theory behind the autonomous approach to sentiment analysis, let’s take a look at the pipeline of this process:
### First step: Pre-Processing.

As we previously discussed, pre-processing procedures, which include tokenization, lemmatization, noise removal, stemming and so forth, “prepare” the text to be read by a computer. 

![_config.yml]({{ site.baseurl }}/images/ml_3.png)

### Second step: Vectorization and Word Embeddings. 

Once the pre-processing is completed, the algorithm converts each word to its binary representation - a *word vector.* 

One way of conducting it is through one-hot vectors, which are basically long sequences of zeros with one 1. These vectors are long and are each represented in a varying way, thus, not allowing a developer to find similarities in numerical representations of the synonyms in the text.

![_config.yml]({{ site.baseurl }}/images/ml_4.png)

The other way of working with word vectors is through *word embeddings.* In word embeddings, the sequences with 0s and 1s are much denser and each contain a lot more information. These numbers are imagined to be plotted on a multidimensional plane, where words in similar meaning are located next to each other. And although this method of word vectorization is mathematically complex, it allows data scientists to keep track of context as much as possible. 

![Alt Text](https://media.giphy.com/media/X9zOFhCdsR8FODDWxV/giphy.gif)

### Third step: Training and Testing the ML model! 

Once the word vectors are determined, the time comes for the deployment of a machine learning model. There’re tons of resources out there to get you started with those, but one thing to make clear is that you won’t have to write a Neural Network by yourself from scratch :)

You’ll be able to use one of the awesome existing Neural Networks - Naive Bayes, SVM, or Random Forest - to first train your machine learning model, and then test it by inputting your own data.

![Alt Text](https://media.giphy.com/media/QGA6c0mlRnglqKXkZZ/giphy.gif)






