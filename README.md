# sms_spam_detecor
Module Challenge 21
📱 SMS Spam Detector 🕵️‍♂️
Overview
This project implements a machine learning solution to classify SMS messages as either legitimate messages (ham) or unwanted messages (spam). Using natural language processing and a Support Vector Machine classifier, the model achieves high accuracy in identifying potentially harmful or annoying spam messages.
Show Image
Features

🤖 Machine learning model using LinearSVC and TF-IDF vectorization
📊 Pre-processing and feature extraction from text data
🌐 Interactive web interface using Gradio
🧪 Example messages to test the system
📈 High accuracy in spam detection

Technologies Used

Python: Core programming language
Pandas: Data manipulation and analysis
Scikit-learn: Machine learning algorithms and evaluation metrics
Gradio: Building the interactive web interface
Natural Language Processing: Text vectorization and feature extraction

How It Works
1. Data Preprocessing
The system uses a dataset of labeled SMS messages (ham/spam) to train a classification model. The text messages are transformed into numerical features using TF-IDF (Term Frequency-Inverse Document Frequency) vectorization:
pythonCopyTfidfVectorizer(stop_words='english')
This technique gives higher weight to words that are unique to specific documents and lower weight to common words.
2. Model Training
The model uses a Linear Support Vector Classification algorithm, which is effective for text classification tasks:
pythonCopyLinearSVC()
The pipeline connects the vectorization and classification steps:
pythonCopyPipeline([
    ('tfidf', TfidfVectorizer(stop_words='english')),
    ('classifier', LinearSVC())
])
3. Interactive Interface
The Gradio interface allows users to:

Enter any text message
Receive an immediate classification (spam or not spam)
Try pre-defined examples

Installation and Usage

Clone this repository:
Copygit clone https://github.com/Daniel956D/sms_spam_detector.git

Install required dependencies:
Copypip install pandas scikit-learn gradio

Run the Jupyter notebook or Python script:
Copyjupyter notebook gradio_sms_text_classification.ipynb

Use the Gradio interface to test the SMS classification.

Example Messages for Testing

"You are a lucky winner of $5000!"
"You won 2 free tickets to the Super Bowl."
"You won 2 free tickets to the Super Bowl. Text us to claim your prize."
"Thanks for registering. Text 4343 to receive free updates on medicare."

Model Performance
The model achieves excellent accuracy in identifying both spam and legitimate messages, with precision and recall metrics substantially above baseline.
Applications
This SMS classification system can be used for:

📧 Personal spam filtering
🔒 Enhanced security against phishing attempts
🏢 Business messaging systems
📊 Analyzing communication patterns

Future Enhancements

Implement more advanced NLP techniques
Add more features based on message metadata
Deploy as a standalone application or API
Add capability to learn from user feedback

Sources and Acknowledgements

SMS Spam Collection Dataset (UCI Machine Learning Repository)
scikit-learn documentation for machine learning implementation guidance
Gradio documentation for building the interactive interface
