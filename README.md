New Analysis Project: Uncover What Matters 


The task was to understand news articles better by doing 3 things: 
  1. Clean up articles 
  2. Check the mood 
  3. Find connections 
These 3 analysis modules were supposed to work as one system together, were 
news articles are given to the system and it returns: 
  1. Mood Rating 
  2. Short Summary 
  3. Big Ideas 
  4. Aspect Analysis (Optional)

So here is the explanation of the working:

The code performs text preprocessing, sentiment analysis, and aspect-based 
sentiment analysis on articles from an Excel file. It also trains a machine learning 
model to classify the sentiment of articles and evaluates its performance. 

1. Import Libraries and Download Resources: The code begins by 
importing necessary libraries including pandas for data manipulation, nltk 
for natural language processing, and sklearn for machine learning. It 
downloads stopwords and VADER lexicon from NLTK.
2. Load Excel File: It loads an Excel file named 'Assignment.xlsx' and 
displays the sheet names. It then loads the data from 'Sheet1' into a 
DataFrame and displays the first few rows. 
3. Clean Articles: A function clean_article is defined to clean text by 
converting it to lowercase, removing punctuation, and removing 
stopwords. This function is applied to the 'Article' column, and the cleaned 
text is stored in a new column 'Cleaned_Article'. 
4. Sentiment Analysis: The code initializes VADER's Sentiment Intensity 
Analyzer. A function check_mood is defined to classify text sentiment as 
Positive, Negative, or Neutral based on VADER's compound score. This 
function is applied to the 'Cleaned_Article' column, and the results are 
stored in a new column 'Mood_Rating'. 
5. Sample Data for Supervised Learning: A sample dataset with labeled 
sentiments is created and combined with the original data for 
demonstration purposes. 
6. Handle Missing Values: The code checks for missing values and removes 
any rows with missing values in 'Cleaned_Article' and 'Mood_Rating' 
columns. 
7. Feature Extraction and Data Splitting: The text data is vectorized using 
TF-IDF, converting it into numerical features. The dataset is split into 
training and testing sets. 
8. Train and Evaluate Model: A logistic regression model is trained on the 
training set and used to predict sentiments on the testing set. The accuracy 
and classification report of the model are printed. 
9. Aspect-Based Sentiment Analysis: A function aspect_analysis is defined 
to analyze the sentiment of specific aspects within the text. It extracts 
sentences containing each aspect, vectorizes them, and predicts their 
sentiment using the trained model. This function is applied to the 
'Cleaned_Article' column, and the results are stored in a new column 
'Aspect_Analysis'. 
10. Save Processed Data: Finally, the processed DataFrame, including aspect 
analysis results, is saved to a new Excel file named 'assignment_processed_with_aspect_analysis.xlsx'.
 

NOTE – I have attached the input file (“Assignment.xlsx”), output 
file(“assignment_processed_with_aspect_analysis.xlsx”) 
and file(“Techdome_Assignment_Code.ipynb”).
