# Movie-Review-Sentiment-Analysis

This project analyzes movie reviews to predict sentiment using multiple approaches including lexicon-based methods and NLP techniques. It also evaluates model performance using standard metrics and performs feature-based sentiment analysis to understand which aspects of movies influence audience opinions.

The main goal is to compare different sentiment analysis techniques, identify the best-performing model, and extract deeper insights from unstructured review text.

## Dataset Features

File: 

MovieReview-Sample.csv
      
      Columns:
              text: Movie review
              label: Actual sentiment (ground truth)
  
  negative-words-LM.txt
  
  positive-words-LM.txt

## Steps taken

### Data Preprocessing:

Cleaned and normalized text data.

Tokenized reviews into words and sentences.

Removed noise and prepared data for analysis.

### Dictionary-Based Sentiment:

Applied Bing Liu sentiment approach using LM word lists.

Used Loughran-McDonald (LM) dictionary.

Calculated sentiment based on positive and negative word counts.

### NLP-Based Sentiment:

Used TextBlob for polarity scoring.

Applied VADER sentiment analyzer for contextual sentiment classification.

### Model Evaluation:

Evaluated all models using Precision, Recall, and F-measure.

Compared performance across positive and negative classes.

### Ensemble Model:

Combined Bing Liu, LM Dictionary, and VADER using majority voting.

Handled tie cases by assigning positive sentiment.

Observed that ensemble reduced overall performance.

### Feature-Based Sentiment Analysis:

Defined features: acting, plot, visuals, and director.

Used sentence-level analysis with VADER.

Calculated sentiment only for sentences mentioning feature keywords.

Assigned feature sentiment as positive, negative, or not mentioned.

### Results:

VADER achieved the highest average F-measure (~0.598).

TextBlob showed strong positive recall but weak negative recall.

Bing Liu and LM Dictionary produced identical results.

Ensemble model reduced performance by ~3.37%.

### Insights:

VADER performs best due to its ability to capture context, negation, and intensity.

Lexicon-based methods struggle with balanced sentiment detection.

Combining weaker models can negatively impact performance.

Acting is the most frequently mentioned and positively reviewed feature.

Other aspects like visuals and direction are mentioned less often but vary in sentiment.

## Install required libraries using:

pip install -r requirements.txt

## Files Included

MovieReviewSentimentAnalysis.ipynb: Jupyter notebook with the complete analysis.

MovieReview-Sample.csv: Dataset.

requirements.txt: List of required Python libraries.

## Tools & Libraries

Libraries: Pandas, NumPy, NLTK, TextBlob, Matplotlib, Seaborn.

Techniques Used: Sentiment Analysis, VADER, Lexicon-Based Methods, Ensemble Modeling, Feature-Based Analysis.

# Author

Reetika Singh



