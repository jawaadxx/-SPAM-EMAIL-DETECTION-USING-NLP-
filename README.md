Spam SMS Detection using NLP Techniques
In this project, the goal was to develop a reliable Spam SMS Detection Model that can classify text messages as either "spam" or "ham" (not spam). With the increase in unsolicited and potentially harmful messages, this project serves as a practical solution to filter out spam effectively, leveraging natural language processing (NLP) techniques and machine learning.

Project Steps
 * Data Loading and Initial Exploration

Dataset: Loaded a dataset containing SMS messages labeled as either spam or ham. The dataset included 5,574 messages with a notable imbalance favoring ham messages.
Class Distribution: Out of all messages, 747 were labeled as spam, while 4,827 were ham.
Missing Values: Confirmed that the dataset had no null values.
Text Preprocessing

 * Lowercasing: Converted all text to lowercase to standardize the input data.
Punctuation Removal: Cleaned the messages by removing punctuation.
Stop Words Removal: Removed common, non-informative words (stop words) to reduce noise in the data.
Stemming and Lemmatization: Reduced words to their base forms for consistency and reduced dimensionality in the model.
 * Data Balancing

Class Balancing: Addressed the class imbalance by undersampling the ham messages to match the count of spam messages, ensuring balanced input for model training.

 * Feature Extraction

Vectorization: Used CountVectorizer to convert the preprocessed text data into a matrix of token counts, transforming the text into numerical data for model compatibility.
Label Encoding: Converted the Class labels to binary values, where spam is represented as 1 and ham as 0.

 * Splitting the Data

Train-Test Split: Split the data into training and test sets (80% training, 20% testing) for reliable model validation.

 * Model Building

Classifier Selection: Chose a Multinomial Naive Bayes classifier, which is well-suited for text data.
Training: Trained the model on the preprocessed training data.

 * Model Evaluation

Accuracy: Achieved a 96% accuracy score on the test data, indicating high effectiveness in distinguishing between spam and ham.
Classification Report: Analyzed precision, recall, and F1 scores, confirming balanced and accurate classification for both spam and ham categories.

 * Confusion Matrix Analysis

Confusion Matrix: Evaluated the model’s performance by examining the confusion matrix:
True Positives (TP): Correctly identified spam messages.
True Negatives (TN): Correctly identified ham messages.
False Positives (FP): Ham messages misclassified as spam.
False Negatives (FN): Spam messages misclassified as ham.
The matrix provided further insights into the model’s reliability, with minimal FPs and FNs, underscoring its suitability for real-world application.

 * Testing with New Messages

Model Testing: To validate real-world applicability, tested the model with new messages, including a promotional offer, which was accurately identified as spam, and a casual personal message, correctly classified as ham.
