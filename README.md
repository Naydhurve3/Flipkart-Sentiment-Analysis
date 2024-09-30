# Sentiment Analysis Project
## Project Overview:
This project performs sentiment analysis on a dataset of reviews, extracting and visualizing insights from the text data. By using Python libraries such as NLTK, Seaborn, Plotly, and WordCloud, we preprocess the text, analyze sentiments (positive, negative, neutral), and create various visualizations to understand the sentiment distribution.

## Dataset:
The dataset consists of a CSV file containing user reviews. The key column in the dataset is:

### `Review`: A text column containing the reviews provided by the users.
The goal of the project is to clean this text data, apply sentiment analysis, and visualize the results. Sentiment analysis will help in understanding the overall tone of the reviews (positive, negative, or neutral).

## Steps Taken:
### 1. Loading and Inspecting the Dataset:

- The dataset is loaded using `pandas` and inspected for any null values. This helps us understand the structure of the data and prepare it for further analysis.
- We used the `isnull().sum()` function to identify missing values, ensuring data quality.
### 2. Text Cleaning:

- Why it was done: Before applying sentiment analysis, text cleaning is essential to remove noise, such as punctuation, numbers, stopwords, URLs, and HTML tags, which could distort the results.
- How it was done: Using regular expressions `(re)` and `nltk`, we cleaned the text by applying transformations like lowercasing, removing punctuation, stopwords, and stemming words to their root forms. The function - `clean()` was applied to the "Review" column to execute this.
- Why this method: Regular expressions provide efficient string matching for filtering out noise. Stemming helps in reducing inflections, leading to more consistent analysis results.
### 3. Rating Distribution Visualization (Bar Chart and Pie Chart):

- Why it was done: To get an initial understanding of how reviews are distributed across different rating categories.
- How it was done: We created a horizontal bar chart using `Seaborn` to visualize the number of reviews per rating. A pie chart was also created using `Plotly` to show the percentage distribution of the ratings.
- Why this method: Bar charts provide a straightforward way to compare review counts, while pie charts offer a quick glance at the proportion of each rating.
### 4. WordCloud for Review Text Visualization:

- Why it was done: To visualize the most frequent words in the reviews, which provides insights into common topics or themes.
- How it was done: The `WordCloud` library was used to generate a word cloud from the cleaned reviews. Frequent words appear larger, while less frequent ones appear smaller.
- Why this method: Word clouds are a visually appealing way to highlight the most common terms, quickly summarizing the content of the reviews.
### 5. Sentiment Analysis (Positive, Negative, Neutral):

- Why it was done: The core task of the project is to analyze the sentiment of the reviews and classify them into positive, negative, or neutral categories.
- How it was done: Using NLTK's `SentimentIntensityAnalyzer`, the polarity scores of each review were computed. New columns were added to store the positive, negative, and neutral scores for each review.
- Why this method: VADER (Valence Aware Dictionary and sEntiment Reasoner) is a highly effective sentiment analysis tool, especially for social media texts and short reviews.
### 6. Sentiment Score Distribution Visualization:

- Why it was done: To visualize the distribution of sentiment scores across all reviews.
- How it was done: A box plot was created using `Seaborn`, showcasing the range of positive, negative, and neutral sentiment scores.
- Why this method: Box plots help identify the spread and outliers of sentiment scores, allowing us to see how sentiments vary across reviews.
### 7. Scatter Plot for Positive vs Negative Sentiment:

- Why it was done: To observe any correlation between positive and negative sentiments in the reviews.
- How it was done: A scatter plot was generated using `Seaborn` to compare positive and negative sentiment scores, with the neutral score as the hue.
- Why this method: Scatter plots provide insights into relationships between variables (positive and negative scores), offering a clear view of how strongly positive or negative reviews are.
### 8. Total Sentiment Calculation:

- Why it was done: To determine the overall sentiment across all reviews, providing an aggregate view of user feedback.
- How it was done: Summing up the positive, negative, and neutral sentiment scores across all reviews, followed by using a custom function `sentiment_score()` to determine which sentiment dominates.
- Why this method: This allows for a simple, intuitive understanding of the general mood in the reviews.
### 9. Visualizing Total Sentiment Scores:

- Why it was done: To display the overall sentiment scores in a bar chart.
- How it was done: A bar plot was created using `Seaborn` to compare the total positive, negative, and neutral sentiment scores.
- Why this method: Bar plots are ideal for comparing discrete values, making it easy to assess which sentiment category has the highest overall score.
## Conclusion:
- By cleaning the text data and performing sentiment analysis, we can gain valuable insights into the overall tone of user reviews. Visualizing this data further helps in understanding patterns and trends in user feedback, allowing businesses to adjust their strategies accordingly. The chosen methods (VADER sentiment analysis, word cloud, box plots, etc.) were selected for their simplicity and effectiveness in handling text-based sentiment data.

## Libraries Used:
- `pandas`: For loading and handling the dataset.
- `nltk`: For text preprocessing and sentiment analysis.
- `seaborn`: For visualizing distributions and relationships.
- `matplotlib`: For generating plots.
- `wordcloud`: For creating word clouds of the reviews.
- `plotly`: For interactive pie charts.
### How to Run:
#### 1. Install the required Python libraries: `nltk`, `pandas`, `seaborn`, `matplotlib`, `wordcloud`, `plotly`.
#### 2. Download NLTK data:
`python`
```
nltk.download('stopwords')
nltk.download('vader_lexicon')
```
#### 3. Run the script to clean the dataset, analyze sentiments, and visualize the results.
