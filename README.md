# week4-sentiment-analyzer
# Sentiment Analysis System
## Overview
This project implements sentiment analysis for product reviews using Natural Language Processing (NLP) techniques from Chapter 23.

## Features
- **Two Analysis Methods:**
- Simple: Word counting based on positive/negative word lists
- Advanced: Machine learning using TextBlob
- **REST API** for easy integration
- **Visualization** of sentiment distributions
- **Text preprocessing** including tokenization and stop word removal
## How to Run
### 1. Install Requirements
        ```bash
        pip install -r requirements.txt
        ```
### 2. Test the Analyzer
        ```bash
        python test_sentiment.py
        ```
### 3. Start the API Server
        ```bash
        python api_server.py
        ```

        Then visit http://localhost:5000

## API Usage Example
```python
import requests
response = requests.post('http://localhost:5000/analyze',
json={'text': 'This product is amazing!'})
print(response.json())
```
## Understanding NLP Concepts
### Tokenization
Breaking text into words: "I love this" → ["I", "love", "this"]

### Stop Words
Common words we filter out: "the", "is", "at", "which"

### Sentiment Analysis
Determining if text is positive, negative, or neutral

## Challenges Encountered
One of my biggest challenges was dealing with Python environment issues. Some of my dependancies were installed to the wrong Python interpreter, which caused import errors and caused half of the project to fail until it was fixed. 

## Real-World Applications
Customer Feedback Analysis: Companies use sentiment analysis to scan large amounts of product reviews or survey data to quickly gauge what the customers like or dislike
Social Media Monitoring: Businesses can track sentiment on social media platforms like Twitter or Reddit to monitor the public opinion about their brand, or any new features.
Customer Support Automation: Sentiment analysis can classify incoming support messages. Urgent or negative messages can be automatically flagged so support teams can respond faster.

## What I Learned
I learned how NLP breaks text down in "Tokens" so it can be analyzed more effectively, and how removing stop words can increase the efficiency of that process. I also gained a better understanding of simple rule-based sentiment systems, and how they are similar/different from machine-learning based tools.