# SMS-Span-Classifier


**Step 1: Importing the Essentials**
- We kick things off by inviting the essential Python libraries to the party. These libraries will help us manipulate and analyze our data. We also bring in our dataset - 'spam.csv' - with the assistance of the trusty pandas library.

**Step 2: Shining a Light on the Data (Data Cleaning)**
- It's like turning on the lights in a dark room! We want to see what we're dealing with. First, we peek at the dataset's info. Then, we're Marie Kondo-ing our DataFrame by tossing out columns we don't need - 'Unnamed: 2', 'Unnamed: 3', and 'Unnamed: 4'. We give our columns friendlier names: 'target' for 'v1' and 'text' for 'v2'. We even put our labels on a diet by encoding them into numbers (0 for ham, 1 for spam).
- Spring cleaning time! We check for missing values and chase away duplicate entries, keeping only the first of its kind.

**Step 3: Uncovering Hidden Gems (Exploratory Data Analysis)**
- Now that our data's spick and span, let's get to know it better! We start by counting how many messages are spammy and how many are pure-hearted 'ham'. A delicious pie chart visualizes this for us.
- But we're not stopping there. We put on our detective hats and analyze:
  - The number of characters in each message.
  - The number of words in each message.
  - The number of sentences in each message.
- We take a peek at these stats separately for ham and spam messages.
- Our data deserves to be seen! We plot histograms and pair plots to give it the spotlight. A heatmap even tells us how features are related.

**Step 4: Preparing for Battle (Data Preprocessing)**
- Before we dive into modeling, we've got to groom our text data:
  - Change everything to lowercase (no need for shouting).
  - Tokenize our text into words.
  - Bid farewell to special characters.
  - Remove pesky stopwords and punctuation.
  - Give words a makeover with stemming (e.g., 'dancing' becomes 'danc').

**Step 5: The WordCloud Show**
- Our data likes to be fancy! We create WordClouds to visualize the most common words in spam and ham messages.

**Step 6: Who's the Top Dog? (Top Words Analysis)**
- Time for a showdown! We analyze and compare the top 30 words in spam and ham messages, showing off the results with snazzy bar plots.

**Step 7: Modeling Madness (Model Building)**
- Now, the real fun begins. We're building models to distinguish between spam and ham messages:
  - We vectorize words using TF-IDF (Term Frequency-Inverse Document Frequency).
  - Split the data into a training team and a testing team.
  - Our contenders include Naive Bayes models like MultinomialNB.
  - We assess their performance using accuracy and precision scores.

**Step 8: Battle Royale (Model Comparison)**
- It's a showdown! Our models fight for supremacy. We pit Support Vector Classifier, K-Nearest Neighbors, Decision Trees, Logistic Regression, Random Forest, AdaBoost, Bagging, Extra Trees, Gradient Boosting, and XGBoost against each other.
- Who wins? We check accuracy and precision to find out.

**Step 9: Fine-Tuning (Model Improvement)**
- We're perfectionists. We try different TF-IDF settings and feature scaling to make our models even better.
- Meet our secret weapons: Voting Classifier and Stacking Classifier. They team up to boost prediction accuracy.

**Step 10: Saving the Best for Later (Model Saving)**
- We don't want to lose our champion models! We save the TF-IDF vectorizer and the Multinomial Naive Bayes model for future use with a pickle.

**Step 11: User-Friendly Prediction (Streamlit Application)**
- Finally, we present our model in a user-friendly Streamlit web application:
  - Users input a message.
  - We clean and preprocess the text.
  - TF-IDF vectorization transforms it into a format our model understands.
  - The model predicts whether it's spam or not.
  - We reveal the result to the user with a flourish!

This code adventure takes us from raw data to a fully interactive tool for detecting spam messages. Enjoy the journey!
