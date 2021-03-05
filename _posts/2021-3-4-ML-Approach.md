---
layout: post
title: Simple Guide to using Machine Learning in Sentiment Analysis Applications 
---

![_config.yml]({{ site.baseurl }}/images/ml.png)


While a rule-based approach to [sentiment analysis](https://saidaibrg.github.io/SA-Definition/) is straightforward and quick, in most cases, it lacks [accuracy](https://www.researchgate.net/publication/329073021_Sentiment_Analysis_and_Feature_Extraction_Using_Rule-Based_Model_RBM_Proceedings_of_ICICC_2018_Volume_2).Therefore, although it’s useful sometimes to know the degree of “positiveness” / “negativeness” of each word, knowing the **[context](https://github.com/yandexdataschool/nlp_course/blob/master/resources/slides/lecture1_word_embeddings.pdf) around a word** is more important. 

Take a look at these tweets:

![_config.yml]({{ site.baseurl }}/images/tweet1.png)

[Twitter - @chakira](https://twitter.com/futuraafreee/status/1361655996368707584)

![_config.yml]({{ site.baseurl }}/images/tweet2.png)

[Twitter - @JeffWysaki](https://www.boredpanda.com/funny-tweets-jeff-wysaski-pleated-jeans-obvious-plant/?media_id=538368)

You, as a human reader, can clearly see that these tweets, despite the words “bomb” and “murderer,” do NOT have any NEGATIVE sentiment. That happens because your [amazing brain](https://www.biorxiv.org/content/10.1101/2020.07.03.186288v1.full.pdf) is able to understand the given text *with* its context and make right conclusions about it. 

Easy-peasy, right?

Well, turns out this is not that of a simple task for computers. However, [machine learning](https://www.youtube.com/watch?v=qoyp8pBtCZ0 ) and neural networks can help to do it.

![_config.yml]({{ site.baseurl }}/images/ml_1.png)

### The biggest difference between a rule-based and ML-based approaches is the role of the **context** for each word. 
In the ML-based sentiment analysis, the [**polarity**](https://ijarcce.com/wp-content/uploads/2012/03/IJARCCE3D-a-Ankush-A-Comparative-Study.pdf ) of every word is determined by taking into account the polarity and lexical meaning of the neighboring words of this token, whereas in a [rule-based](https://saidaibrg.github.io/Sentiment-Analysis/) method only a polarity of a specific word is calculated.  

To understand the theory behind the [autonomous approach](https://www.digitalocean.com/community/tutorials/how-to-perform-sentiment-analysis-in-python-3-using-the-natural-language-toolkit-nltk) to sentiment analysis, let’s take a look at the pipeline of this process:
### First step: Pre-Processing.

As we [previously discussed](https://saidaibrg.github.io/Sentiment-Analysis/), pre-processing procedures, which include [tokenization](https://www.pluralsight.com/guides/building-a-twitter-sentiment-analysis-in-python), lemmatization, noise removal, stemming and [so forth](https://github.com/fastai/course-nlp/blob/master/2-svd-nmf-topic-modeling.ipynb), “prepare” the text to be read by a computer. 

![_config.yml]({{ site.baseurl }}/images/ml_3.png)

### Second step: Vectorization and Word Embeddings. 

Once the pre-processing is completed, the [algorithm](https://algorithmia.com/blog/using-machine-learning-for-sentiment-analysis-a-deep-dive) converts each word to its binary representation - a *word vector.* 

One way of conducting it is through [one-hot vectors](https://towardsdatascience.com/word-embeddings-for-sentiment-analysis-65f42ea5d26e), which are basically long sequences of zeros with one 1. These vectors are long and are each represented in a varying way, thus, not allowing a developer to find similarities in numerical representations of the synonyms in the text.

![_config.yml]({{ site.baseurl }}/images/ml_4.png)

The other way of working with word vectors is through [*word embeddings.*](https://web.stanford.edu/~jurafsky/slp3/) In word embeddings, the sequences with 0s and 1s are much denser and each contain a lot more information. These numbers are imagined to be plotted on a multidimensional plane, where words in similar meaning are located next to each other. And although this method of word vectorization is [mathematically complex](https://github.com/yandexdataschool/nlp_course/tree/master/week01_embeddings), it allows data scientists to keep track of context as much as possible. 

![Alt Text](https://media.giphy.com/media/X9zOFhCdsR8FODDWxV/giphy.gif)

### Third step: Training and Testing the ML model! 

Once the word vectors are determined, the time comes for the deployment of a machine learning model. There’re tons of [resources out](https://github.com/fastai/course-nlp) there to get you started with those, but one thing to make clear is *that you won’t have to write a Neural Network by yourself from scratch* :)

You’ll be able to use one of the awesome [existing Neural Networks](https://www.linkedin.com/pulse/best-ai-algorithms-sentiment-analysis-muktabh-mayank/) - Naive Bayes, [SVM](https://www.researchgate.net/publication/342221481_Comparison_of_Naive_Bayes_and_SVM_Algorithm_based_on_Sentiment_Analysis_Using_Review_Dataset), or Random Forest - to first [train](https://www.kdnuggets.com/2018/08/emotion-sentiment-analysis-practitioners-guide-nlp-5.html) your machine learning model, and then test it by inputting your own data.

![Alt Text](https://media.giphy.com/media/QGA6c0mlRnglqKXkZZ/giphy.gif)






