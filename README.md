# Combining Topic and Sentiment Analysis on Articles about Artificial Intelligence from Varying Media Outlets

Assignment 2 for the course 'Critical Data Mining of Media Culture' [INFOMCDMMC] as part of the MSc Applied Data Science programme at Utrecht University. In this research, we combine topic and sentiment analysis on a dataset of articles about AI and other AI-related subjects from 5 different media outlets to determine in what ways the sentiment differs per discussed topic in the media.

Files:

1. Loading_and_Cleaning.ipynb : in this file, we clean the dataset by removing contents such as 'No description found' or 'No content found'. Also, we explore the dataset in this file by displaying and counting how many articles each outlet has published over the years, including determining whether or not in particular months more articles get published. We also evaluate which media outlet is included more often in the dataset. From this information, we can determine to what extent the data may be (im)balanced.

2. Preprocessing.ipynb : in this file, we use functions such as do_nlp, include_features and clean_text to eleminate irrelevant words from the dataset (in both the bodies and descriptions). This preprocessed data is saved to a csv file so we can use it for future analyses.

3. LDA.ipynb : in this notebook we perform two different types of LDA analyses. In this notebook, the preprocessing steps are also included though. In the later stages of the analysis, we relocated the preprocessing steps to a separate notebook (Preprocessing.ipynb), and since we did not progress with LDA, the preprocessing steps were not excluded.

4. KMeans.ipynb : in this notebook, we determine the optimum number of clusters per media outlet with methods such as TF-IDF and KneeLocator. Subsequently, with the optimum number of clusters, we determine the topics.

5. Sentiment_TextBlob.ipynb : includes the sentiment analysis conducted on both the bodies and the descriptions with TextBlob. For TextBlob, we also did two types of sentiment analyses: one with the standard TextBlob sentiment function, and another where we manually edited the cutoff points. These custom-made cutoff points were created to identify whether or not this might balance the sentiment distribution a bit. Cutoff points are, after all, sometimes recommended in case the sentiment classifier produces somewhat biased results towards particular sentiment(s).

6. Sentiment_Vader.ipynb : includes the sentiment analysis conducted on both the bodies and the descriptions with VADER

7. Compare_Sentiments.ipynb : in this notebook we compare the sentiment labels given manually by each team member. We calculate the percentage of articles on which these manual labels agreed with the sentiments given by TextBlob and VADER.

8. Presentation_slides.pdf : the slides used for the presentation in our research project.

9. Combined_Sentiment_Topics.ipynb : includes the combined analysis of sentiment and topic. In this notebook, we give label names to the topics, and then we plot the sentiment for each topic that we identified per outlet.
