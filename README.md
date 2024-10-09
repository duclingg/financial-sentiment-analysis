# Financial Sentiment Analysis

In this program I create a tool that will help predict the price movement of a publicly-traded company's stock, based on the sentiment from news articles mentioning that company, as well as other financial indicators such as stock price.  

By collecting and cleaning news articles, I can then perform the sentiment analysis in regards to the company. And then I can gather important financial data and indicators.  

After data collection and sentiment analysis, I can build models which determine the correlation between the different data sets, and train a machine learning model to create a tool which will determine the price movement of that stock.

### For easier access viewing and a detailed breakdown of the code: [Jupyter Notebooks](jupyter/notebooks)  
In these notebooks, I am researching and developing the main scope of the tool. I go through the necessary steps in preparing the data for the building and training the model before implementing it in a tool.  

**Part 1:**  
[Data Extraction and Collection](jupyter/notebooks/single-analysis-pt1.ipynb)  

**Part 2:**  
[Data Preprocessing](jupyter/notebooks/single-analysis-pt2.ipynb)  

**Part 3:**  
[Sentiment Analysis and Data Merging](jupyter/notebooks/single-analysis-pt3.ipynb)  

**Part 4:**  
[Data Analysis](jupyter/notebooks/single-analysis-pt4.ipynb)

**Part 5:**  
[Model Building and Evaluation] **In progress**  

#### If you would like to run these notebooks on your own machine:  
1. After cloning the repository, create a folder in the root called `config`  
2. Create a file called `.env` in `config`, and create a variable in the file called `NEWS_API_KEY`  
3. Get your `NewsAPI` key from [newsapi.org](https://newsapi.org)
4. Download the necessary packages:
    - I recommend creating a Python virtual environment (.venv) running 3.11.5, activate the environment and `pip install`: 
    - `os`, `dotenv`, `datetime`, `newsapi`, `pandas`, `re`, `string`, `transformers`, `torch`, `yfinance`, `matplotlib`, `seaborn`, `scipy`, `sklearn`

## What is Sentiment Analysis?
Also known as opinion mining, it is the process of analyzing large volumes of text to identify and extract subjective information. It is the most common text classification tool to analyze the underlying sentiment; whether that is postive, negative, or neutral.  

**Rule-based Sentiment Analysis**  
Software is trained to classify certain keywords in a block of text based on groups of words (lexicons), that describe the authors intent. Lexicons will have different sentiments (positive, negative, neutral), in which the software will scan the classifier for the words in either the positive or negative lexicon, tallying up the total sentiment score based on the volume of words used and the score for each category.  

**Machine Learning Sentiment Analysis**  
An algorithm is used to train software to gauge sentiment in a block of text, using words that appear in the text as well as the order in which they appear. The goal is to teach software how to identify emotion in text similarly to the way humans do.  

In this program, we use a combination of both, a hybrid approach. We use pretrained models (`NLTK`) to calculate the sentiment scores of the articles (rule-based). Then with the financial data, we will train our own machine learning model to gauge the sentiment as it relates to the financial data.

## Correlation Analysis
From the data that we collected, cleaned, and ran sentiment analysis on, we can find the correlation between the sentiment of the articles and the financial data/indicators.  

By finding the correlation between the two separate data sets, we can visualize the correlation using graphs, plots, etc., in which we can try to draw conclusions from; such as whether or not there is a relationship between them.  

**Note: Correlation DOES NOT equal causation**  
Rather, it just quanitifies the strength of the relationship between the features of a dataset.  

## Building and Training the Model

