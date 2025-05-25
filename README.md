 Emotion Classification with SVM
This project performs emotion classification on text using a Support Vector Machine (SVM) model. It includes tweet scraping, preprocessing, clustering (unsupervised learning), model training, performance evaluation, persistence, and an optional alert system.

 Project Structure

├── emotions.csv                # Main dataset (pre-labeled)
├── best_svm_model.pkl          # Saved best-performing SVM model
├── tfidf_vectorizer.pkl        # Saved TF-IDF vectorizer
├── label_encoder.pkl           # Saved label encoder
├── emotion_classifier.py       # Main code file (or .ipynb if notebook)
└── README.md                   # This file
⚙️ Features
✅ 1. Tweet Scraping (Real-Time)
Uses snscrape to fetch tweets matching emotional keywords (happy, sad, angry, etc.).

Saves them in a DataFrame for classification.

✅ 2. Text Preprocessing
Lowercasing, URL/user/hashtag removal

Punctuation and number cleaning

Stopword removal

Stemming using PorterStemmer

✅ 3. Clustering (KMeans)
Applies KMeans clustering to scraped tweets (unsupervised learning)

Helps detect patterns or emotional clusters without labels

✅ 4. SVM Classification
Trains multiple SVM models using different kernels: linear, poly, rbf, and sigmoid

Evaluates using accuracy, precision, recall, and F1-score

Visualizes confusion matrices

✅ 5. Model Persistence
Saves:

Best SVM model (best_svm_model.pkl)

TF-IDF vectorizer (tfidf_vectorizer.pkl)

Label encoder (label_encoder.pkl)

✅ 6. Optional Alerting System
Flags and prints alerts for negative emotions (e.g., sad, angry) from scraped tweets

📈 Best Model Summary
Kernel	Accuracy	F1-Score
Linear	0.874	0.873
Sigmoid	0.873	0.872
RBF	0.856	0.852
Poly	0.644	0.602

➡️ Best Performing Kernel: linear
