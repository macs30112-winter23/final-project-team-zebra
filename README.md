# Abortion as a Public Issue: A Sentiment Analysis of Social Media versus Popular Media

## Summary
### Project Goal: Objective of the Project and Rationale

The objective of our project is to study the difference in views about abortion, on social media versus in popular media between January 2022 and January 2023. 

Social science research suggests that views about abortion can differ on social media and in popular media, with social media tending to amplify extreme views and popular media presenting a more nuanced view of the issue. It's important to be aware of these differences and to seek out a range of perspectives when engaging in discussions about abortion. Our project aims to help understand and deconstruct these differences through data visualizations, observations from data, and data modeling.

### Social Science Perspective, Research Questions, and Hypotheses

The question of whether abortion should be legal or not has led to the creation of two main groups: pro-choice and prolife. However, just recently, the Supreme Court of the United States (SCOTUS) officially overturned the Roe vs. Wade case on June 24, 2022. The Roe vs. Wade case first appeared in court in 1973 and was a landmark decision that stated that the Constitution of the United States granted citizens the right to an abortion. However, with the recent overturning, abortion rights are now decided by each individual state on whether it is a right or not.

With the multitude of opinions in popular media and on social media, our project seeks answer to the following questions:
* How are people reacting to the topic of abortion online, particularly on Twitter?
* Are there any geospatial trends in where Tweets are posted from? Can we group states by their views on social media?
* What are the views being expressed through popular media, such as newspapers like the New York Times? Are views in popular media ‘milder’ (more neutral) than those on social media?
* Can the data from these observations be modeled or visualized to gather further insights and draw out parallels between the two channels of expression?
* Is there a difference between these observations after the June 2022 ruling?

Based on social science research in the past, we *hypothesized* that social media tends to amplify extreme views on abortion. On the other hand, popular media, such as newspapers like The New York Times, tend to present a more nuanced view of abortion. We expect a similar result after carrying out a ‘sentiment analysis’ on both sources (more details on this follow). While media outlets may have their own editorial biases, they often present a range of perspectives on the issue of abortion and the various political and social factors that contribute to it.

We scrape data from Twitter and the New York Times to carry out a sentiment analysis (through the pre-trained [RoBERTa-Base Model](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment)) to gather insights and provide answers to these questions.

### Main Findings

**Results of the sentiment analysis showed that:**
* Overall, Tweets show a greater extent of extreme sentiments – particularly negative sentiment, across all four major cities we studied 
* On the other hand, the New York Times articles (both headlines and lead bodies) generally showcase ‘milder’ sentiments, such that a more neutral sentiment can be observed for them, across the time-period we studied (important to note here that positive sentiment is not observed in both cases)

**Effect of the June 2022 ruling:**
* Our analysis showcase that the effect of the 2022 ruling was evident in the way the word ‘abortion’ appeared in both, Tweets and NYT articles: while there was an increase in volume of both, Tweets as well as articles, the net effect was convergent to the effect seen in general: negative sentiments for Tweets, and neutral for articles 
* There can be observed a peak in negative sentiment Tweets at the time of the overruling, and a synchronous peak of neutral sentiment headlines in NYT around this same time period - which ratifies our conclusions so far

**Geographic incidence of views on social media:**
* We also observe that there is a difference in the way sentiments are expressed, on a geographic basis. We studied 4 large US cities. The number of positive sentiment Tweets were distributed as: New York > Chicago > Seattle > Los Angeles

## List of Data Sources

*Further details regarding these, as well as the project (with feedback incorporated) can be found in the updated project report here, the updated project slides here, and the project video here.*

Data Source 1: Pregnancies, Births and Abortions in the United States: National and State Trends
* Type of data collection: downloading open source data by the Guttmacher Institute available [here](https://osf.io/kthnf/)
* Time frame: 1988 to 2017
* Size of the dataset: ~ 1000 observations across states over the years

Data Source 2: Tweets related to abortion views
* Type of data collection: scraping using a Python library called `snscrape` that allows us to scrape Tweets by defining key words, time periods, geographical information and other advanced search parameters
* Time frame: January 2022 to January 2023
* Size of the dataset: ~ 8500 Tweets 

Data Source 3: New York Times articles related to abortion
* Type of data collection: web scraping by integrating the NYT API
* Time frame: January 2022 to January 2023
* Size of the dataset: ~500 articles

## Python Libraries Used
* `Snscrape`: version 0.3.5
* `Scikit-learn (sklearn)`: version 1.0.1
* `NLTK (Natural Language Toolkit)`: version 3.6.2
* `TextBlob`: version 0.15.3
* `NumPy`: version 1.21.2
* `Pandas`: version 1.3.3
* `Transformers`: version 4.11.3
* `PyTorch`: version 1.9.0
* `SciPy`: version 1.7.1
* `Time`: built-in module, no version number
* `Datetime`: built-in module, no version number
* `Dateutil`: version 2.8.2
* `Statsmodels`: version 0.13.0
* `Requests`: version 2.26.0
* `Beautiful Soup (bs4)`: version 4.10.0
* `Matplotlib`: version 3.4.3
* `Seaborn`: version 0.11.2
* `Plotly.express`: version 0.4.1
* `Wordcloud`: version 1.8.1

## Navigating this Repository 
Find the detailed documentation regarding the project under the **Documentation** folder. Follow this order of steps to replicate the code:
* Beging with the **Twitter_DataProcessing** folder which has two Jupyter Notebooks (Part I and Part II) that carry out the data collection, cleaning/wrangling, analysis, and some basic visualizations for the Tweets.
* Move on to the **NYT_DataProcessing** folder which has one Jupyter Notebook that does the same steps for the New York Times data.
* The **Data_Files** folder collates all the collected and processed data used for this project.
* The **DataAnalysis_and_Visualization** folder carries a Jupyter Notebook which creates the final visualizations for the project. 
* Lastly, the **Trial Code** folder has some Jupyter Notebooks from the initial phases of the project where we explored some of the tasks we have carried out in this project.
* You may refer to the **requirements.txt** file for system requirements that may be needed to run the code. 

### Thanks for visiting our repository!
