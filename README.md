# SMS Spam Classifer
**The aim of this model is to classify this incoming SMS as either "spam" or "ham" (legitimate message).**

The following are the techniques that are used in the model:

1] Data Preprocessing: 
- Text Cleaning: Removing irrelevant symbols like punctuation, extra spaces, and emojis.
- Normalization: Converting all text to lowercase for case-insensitive analysis.
- Lemmatization: Reducing words to their base form (e.g., "winning" becomes "win"). This helps capture the meaning regardless of tense or conjugation.

2] Feature Engineering: This transforms the cleaned message text into numerical features that a machine learning model can understand. Here we used the following techniques:
- Count Vectorizer (Bag of Words): This method creates a vocabulary of unique words encountered in the training data. Each message is then represented as a vector where each element indicates the frequency of a corresponding word in the message. 
- TF-IDF Vectorizer: It considers not just word frequency but also how common a word is across all messages. Words that are very frequent overall (e.g., "the", "a") get lower weightage, while words specific to spam messages get a higher TF-IDF score, leading to a more informative representation.
- Word Cloud: Counting the occurrences of each word in the message. Words frequently appearing in spam (e.g., "FREE", "WIN") get higher weightage.

3] Machine Learning Model: Here we utilized two pre-trained machine learning models specifically designed for text classification. This model has been trained on a dataset of labeled SMS messages (spam and ham) and can recognize patterns that differentiate between the two categories.
- Naive Bayes: A popular algorithm for spam filtering due to its efficiency and effectiveness in classifying text based on word probabilities.
- Support Vector Machines (SVM): Powerful for handling high-dimensional data created from features like word frequency. It also achieves more accuracy.

4] Model Evaluation: Here we create comfusion matrix and use the classification report function to evaluate oour model using Accuracy, Recall and F1 scores.

5] Making Predictions: In this model we gave unknown input text and the model predicts if it is a spam message or a ham message(legitimate)

**Thus this model can help protect from unwanted promotional messages, phishing attempts, or other malicious content.**
