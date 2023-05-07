# Sentiment-analysis-of-ChatGPT-Tweets-using-VADER-and-RoBERTa

Introduction:
ChatGPT is an artificial intelligence chatbot developed by OpenAI. Soon after its release in November 2022, ChatGPT has become the talk of the town for its detailed responses and articulated answers across various domains of knowledge. Many people and organizations are speaking in favour of this artificial intelligence. However, not everyone is a fan. People are sharing their thoughts about this AI tool on different social media platforms like Twitter and more. To compare the results of two different models, in this project, sentiment analyses are performed using the VADER and RoBERT models on the tweets posted regarding ChatGPT.

Tools and technique used: Python(Pandas, Numpy, NLTK, Transformer), Power Bi (data visualisation tool)

I used the NLTK Python library, since it already has a built-in, pretrained sentiment analyzer called VADER (Valence Aware Dictionary and Sentiment Reasoner).

As VADER is pretrained, you can get results more quickly than with many other analyzers. VADER is best suited for the short sentences, slang, and abbreviations seen in social media. Although it is less reliable when grading larger, more organized sentences, it is frequently a useful starting point.

For comparison, I used RoBERTa (Robustly Optimized BERT-Pretraining Approach), which pre-trained moddel by hugging faces. RoBERTa is trained on a massive dataset that spans over 160GB of uncompressed text. RoBERTa is trained for longer sequences, but it is really time-consuming.

Results:

After using both analyses, it is clear that nearly 18% of tweets about ChatGPT were negative, and 72% of tweets were either positive or neutral.

In the analysis by the VADER model, the maximum number of tweets were positive; however, in the analysis by the RoBERTa model, tweets were mostly neutral.
![](https://github.com/Devendrasingh8/Sentiment-analysis-of-ChatGPT-Tweets-using-VADER-and-RoBERTa/blob/main/VADER%20Model-%20Sentiment%20Analysis.png)

It is interesting to note that not all tweets tagged as positive by the VADER model were categorized as positive by the RoBERTa model. And the same is true for other sentiments that are negative or neutral.

Out of the tweets that were tagged negative by the VADER model, only about 50% were tagged negative. However, nearly 13% and 37% of those tweets were reported positively and neutrally by the RoBERTa model, respectively. Similarly, you can see the composition of RoBERTa sentiment analysis in neutral and positive VADER tweets.

Interpretation:

To understand these results better, let us understand how these two models work. VADER sentiment analysis primarily uses a lexicon that converts lexical characteristics into sentiment scores, a measure of the strength of an emotion. By adding the intensity of each word in a text, it determines the sentiment score of that text. However, RoBERTa is trained on a massive dataset of over 160GB of uncompressed text, and it is trained with full sentences. This transformer not only accounts for words but also the context related to other words. This model can show the polarity of the overall idea of the author. It can also guess sarcasm and hidden criticism.

It can be seen that the first two tweets are positive, but they were given negative sentiment by VADER analysis, but after doing RoBERTa analysis, we got positive sentiment as a result. and the opposite has happened in the following three overall negative tweets.

We saw in the samples above that RoBERTa's accuracy is far greater and more realistically reflective. Yet there are other factors that play a role in data science beyond accuracy. One criterion for a model is that it should be as computationally light as feasible, especially for production, because time is an important resource.

It is clear that VADER is significantly simpler to use than RoBERTa. Moreover, VADER outruns RoBERTa in terms of speed. On my PC, VADER accurately anticipated the emotion of 200K tweets in under 2 minutes. In contrast, RoBERTa completed the same task in more than 6 hours.

Conclusion:

There is no magic solution, but one can choose between RoBERTa or VADER based on the task and the available computational resources. Twitter-RoBERTa, on the other hand, appears more promising, especially if the volume of data is not as large, thanks to its little pre-processing of the data and astounding accuracy. RoBERTa analysis gives a upper hand while analysing sentiments of the large text; however, it is very slow compared to VADER.

Keywords:
Sentiment Analysis: attempt to extract subjective qualities—attitudes, emotions, sarcasm, confusion, and suspicion—from text.
NLTK: Natural Language toolkit
VADER: (Valence Aware Dictionary and sEntiment Reasoner)
RoBERTa: (Robustly Optimized BERT-Pretraining Approach)
Lexical Feature: Any feature that we use for written communication.
