# 📧 Spam Email Classifier

A machine learning project that classifies emails as **Spam** or **Ham (Not Spam)** using **Natural Language Processing (NLP)** and a **Random Forest Classifier**.

---

## 🚀 Overview

This project builds a text classification pipeline that:
1. Cleans and preprocesses raw email text (lowercasing, punctuation removal, stopword removal, stemming).
2. Converts the cleaned text into numerical features using **Bag-of-Words (CountVectorizer)**.
3. Trains a **Random Forest** model to classify emails as spam or ham.
4. Achieves **~97.7% accuracy** on the test set.
5. Demonstrates predicting the label of a new/unseen email.

---

## 🧠 How It Works

**Pipeline steps:**

| Step | Description |
|------|-------------|
| 1️⃣ Load Data | Reads `spam_ham_dataset.csv` into a pandas DataFrame |
| 2️⃣ Clean Text | Removes line breaks, punctuation, and converts to lowercase |
| 3️⃣ Remove Stopwords | Filters out common English stopwords using NLTK |
| 4️⃣ Stemming | Reduces words to their root form using `PorterStemmer` |
| 5️⃣ Vectorization | Converts text into numeric vectors with `CountVectorizer` |
| 6️⃣ Train/Test Split | Splits data (80% train / 20% test) |
| 7️⃣ Model Training | Trains a `RandomForestClassifier` |
| 8️⃣ Evaluation | Scores the model on the test set |
| 9️⃣ Prediction | Classifies a sample email as spam or ham |

---

## 📂 Project Structure

```
spam-email-classifier/
│
├── SpamEmail.ipynb          # Main Jupyter Notebook (full pipeline)
├── spam_ham_dataset.csv     # Dataset (emails labeled as spam/ham)
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation
└── .gitignore                # Ignored files/folders
```

---

## 🛠️ Tech Stack

- **Python 3**
- **pandas** — data handling
- **NLTK** — text preprocessing & stopwords
- **scikit-learn** — vectorization, train/test split, Random Forest model

---

## ⚙️ Installation & Usage

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/spam-email-classifier.git
   cd spam-email-classifier
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download NLTK stopwords** (only needed once — the notebook also does this automatically)
   ```python
   import nltk
   nltk.download('stopwords')
   ```

4. **Run the notebook**
   ```bash
   jupyter notebook SpamEmail.ipynb
   ```

> ⚠️ Make sure `spam_ham_dataset.csv` is in the same directory as the notebook before running.

---

## 📊 Results

| Metric | Score |
|--------|-------|
| Accuracy | **97.7%** |

The model correctly classified a sample email from the dataset, matching the true label.

---

## 🔮 Future Improvements

- [ ] Try **TF-IDF** instead of raw Bag-of-Words for potentially better feature weighting
- [ ] Compare Random Forest against other models (Naive Bayes, SVM, Logistic Regression)
- [ ] Add a confusion matrix and classification report for deeper evaluation
- [ ] Wrap the model in a simple script/CLI or web app (Flask/Streamlit) for real-time predictions
- [ ] Save the trained model with `joblib`/`pickle` for reuse without retraining

---

## 👩‍💻 Author

**Nourhan**
Computer Science & AI student | Content creator [@codewithnour](https://instagram.com/codewithnour)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
