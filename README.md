## Data Problem Statement

   **FAKE NEWS is a problem:**
   In the era of Social Media where news spread is just one click away, fake news spreads quicker and further than ever.

   **Perception**
   According to a Pew Research Center survey:
   -Americans rate it as a larger problem than racism, climate change, or terrorism.
   -Nearly 60 percent of Democrats have dropped an outlet over perceived fake news, and a full 70 percent of Republicans have

   **Reality**
   Fake news is not actually as prevalent nor influential as thought
   A recent Princeton-led study of fake news consumption during the 2016 campaign found that false articles made up 2.6 percent of all hard-news articles late in the 2016 campaign, with the stories most often reaching intense partisans who probably were not persuadable.

   **The **

   **Yet this problem is not easily solved for several reasons:**
   1. The sheer amount of news being generated daily
   2. Limited number of fact checkers


   **From a data science perspective:**  

OPPORTUNITY:
Where human fact checkers might be overwhelmed, processing the amount of news being generated is exactly the forte of modern day computing

CHALLENGE:
The limited number of fact checkers however, mean that there may be a lack of labeled data to work with and this presents a non-trivial problem: machine learning works best with clearly labeled data (i.e. supervised learning).

   On further research, two main categories of datasets were found:

|Dataset|Dataset Type A|Dataset Type B|
|--|--|--|
|Source|Fact-checking websites, eg.Snopes, Politifact|Datascrapers|
|Size|Tens to thousands|Millions|
|Categorization|Individually|By domain trustworthiness|
|Topic Range|Tend to be focused on one specific topic, i.e. US politics or celebrities|Wide range|


Each dataset type presents its own challenges and opportunities. Type A datasets are clearly labeled, and have been done so by largely apolitical groups. Unfortunately, these datasets tend to be small, as the effort to do these fact checks is large, and aforementioned lack of fact-checkers. The topic range also tends to be much smaller, and may not generalize to news outside of this data.

Type B datasets on the other hand, are extremely large, which is important for text-classification tasks, but are labeled simply by the trustworthiness of the domain judged as a whole. We want a model that is generalized to detect fake news, not just the specific style of a news source, which could be the result of training on such data. On the other hand the wide range of topics at hand gives a better generalization to unseen news.

In this project, we look at one dataset of each kind:

**Type A dataset: MisInfoText, Buzzfeed Dataset (2019)**
    Fatemeh Torabi Asr and Maite Taboada (2019) MisInfoText. A collection of news articles, with false and true labels. Dataset.

The data for this source was first taken from various Facebook groups by three Buzzfeed reporters, and were labeled with 4 classes:

        -Mostly True
        -Mixture of True and False
        -Mostly False
        -No Factual Content

The authors of this dataset then followed the URLs in the first dataset, and scraped the full text of each news article from its original source. The resulting dataset includes a total of 1380 news articles on a focused topic (US election and candidates). Veracity labels come in a four-way classification scheme including 1090 mostly true, 170 mixture of true and false, 64 mostly false and 56 articles containing no factual content.

| Type | Count |
| ------------- |:-------------:|
| **Mostly True** | 1090|
| **Mixture of True and False** |  170 |
| **Mostly False** |  64|
| **No Factual Content** |  56 |

**Type B: Fake News Corpus**

This is an open source dataset composed of millions of news articles mostly scraped from a curated list of 1001 domains from http://www.opensources.co/. Because the list does not contain many reliable websites, additionally [NYTimes](https://developer.nytimes.com/) and [WebHose English News Articles](https://webhose.io/datasets) articles has been included to better balance the classes.

Opensources.co contained a list of 1001 domains and classified them by 11 different categories of fake news, described in the following:

| Type | Tag | Count (so far) | Description|
| ------------- |:-------------:|:-------------:|:-------------:|
| **Fake News** | fake | 928,083 | Sources that entirely fabricate information, disseminate deceptive content, or grossly distort actual news reports |
| **Satire** | satire | 146,080 | Sources that use humor, irony, exaggeration, ridicule, and false information to comment on current events. |
| **Extreme Bias** | bias | 1,300,444 | Sources that come from a particular point of view and may rely on propaganda, decontextualized information, and opinions distorted as facts. |
| **Conspiracy Theory** | conspiracy | 905,981 | Sources that are well-known promoters of kooky conspiracy theories. |
| **State News** | state | 0 | Sources in repressive states operating under government sanction. |
| **Junk Science** | junksci | 144,939 | Sources that promote pseudoscience, metaphysics, naturalistic fallacies, and other scientifically dubious claims. |
| **Hate News** | hate | 117,374 | Sources that actively promote racism, misogyny, homophobia, and other forms of discrimination. |
| **Clickbait** | clickbait | 292,201 | Sources that provide generally credible content, but use exaggerated, misleading, or questionable headlines, social media descriptions, and/or images. |
| **Proceed With Caution** | unreliable | 319,830 | Sources that may be reliable but whose contents require further verification. |
| **Political** | political | 2,435,471 | Sources that provide generally verifiable information in support of certain points of view or political orientations. |
| **Credible** | reliable | 1,920,139 | Sources that circulate news and information in a manner consistent with traditional and ethical practices in journalism (Remember: even credible sources sometimes rely on clickbait-style headlines or occasionally make mistakes. No news organization is perfect, which is why a healthy news diet consists of multiple sources of information). |

Part 1 of the project deals with the Type A dataset example, which is focused on classifying news within a particular domain, in this case, 2016 American Politics.

Part 2 of the project deals with using Type B datasets to classify news websites outside of the dataset.


github
[Github Repo](https://github.com/tynlong/FakeNewsClassification.git)
## Acknowledgments
- [http://www.opensources.co/](http://www.opensources.co/)
- [NYTimes Developer](https://developer.nytimes.com/)
- [WebHose](https://webhose.io/datasets)
- Fatemeh Torabi Asr and Maite Taboada (2019) [MisInfoText](https://github.com/sfu-discourse-lab/MisInfoText). A collection of news articles, with false and true labels. Dataset.
# FakeNewsClassification
# FakeNewsClassification
# FakeNewsClassification
