<H3>ENTER YOUR NAME:MATHESWARAN K</H3>
<H3>ENTER YOUR REGISTER NO: 212222110024</H3>
<H3>DATE:11.5.24</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:Perform sentiment analysis using your Facebook data and filter the data that has only neutral feedback for the code given in the following link<H3>
<H3>Program:</H3>

```
import pandas as pd
from textblob import TextBlob

# Load your Facebook data from CSV into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Filter the DataFrame to include only rows with neutral sentiment
neutral_feedback = df[df['Sentiment'] == 0]  # Sentiment polarity of 0 indicates neutral sentiment

# Output the neutral feedback
print("Neutral Feedback:")
print(neutral_feedback)

```

<H3>Output:</H3>

![image](https://github.com/mathes6112004/Project-Based-Experiment-AAI/assets/119477782/b997a463-3c81-4e33-be30-1cdc98849d0f)
![image](https://github.com/mathes6112004/Project-Based-Experiment-AAI/assets/119477782/1b35d54d-5ad1-4401-acb0-a1bc814bc207)

<H3>Inference:</H3>
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only neutral feedback for the code is done.
