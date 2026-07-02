# 📧 Spam Email/SMS Detection using Support Vector Machine (SVM)

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikitlearn&logoColor=white" alt="Scikit-Learn">
  <img src="https://img.shields.io/badge/Model-SVM-9cf" alt="SVM">
  <img src="https://img.shields.io/badge/Accuracy-98.2%25-brightgreen" alt="Accuracy">
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License">
</p>

<p align="center">
  A machine learning project that classifies email/SMS messages as <b>Spam</b> or <b>Not Spam</b>
  using a <b>Support Vector Machine (SVM)</b> classifier trained on TF-IDF text features.
</p>

<p align="center">
  <a href="https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/spam_classifier_svm.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">
  </a>
</p>

---

## 📌 Overview

Spam messages are a major nuisance and security risk. This project builds a **text classification pipeline** that automatically detects spam messages using classical NLP + Machine Learning techniques.

The pipeline:
1. Cleans and preprocesses raw text
2. Converts text into numerical features using **TF-IDF Vectorization**
3. Trains a **linear-kernel SVM** classifier
4. Evaluates performance with accuracy, precision, recall, and F1-score
5. Lets users interactively type in a message and get an instant **Spam / Not Spam** prediction

---

## 🎯 Demo

```
==================================================
 SPAM DETECTOR - Enter a message to classify it
 (type 'exit' or 'quit' to stop)
==================================================

Enter an email/message text: Congratulations! You won a free lottery prize, claim now
Prediction: SPAM  (confidence: 96.42%)

Enter an email/message text: Hey, are we still meeting for lunch tomorrow?
Prediction: NOT SPAM  (confidence: 94.18%)
```

---

## 📊 Dataset

| Property        | Details                                   |
|------------------|-------------------------------------------|
| **File**         | `spam_mail.csv`                           |
| **Rows**         | 5,572 messages                            |
| **Columns**      | `Category` (ham/spam), `Masseges` (text)  |
| **Class Split**  | 4,825 Ham • 747 Spam                      |

> The dataset is a labeled collection of SMS/email messages tagged as either `ham` (legitimate) or `spam`.

---

## 🧠 Model & Approach

| Step                  | Technique                                  |
|------------------------|---------------------------------------------|
| Text Cleaning          | Lowercasing, URL/number/punctuation removal |
| Feature Extraction     | TF-IDF Vectorizer (`stop_words='english'`)  |
| Classifier              | Support Vector Machine (`kernel='linear'`)  |
| Class Imbalance Handling | `class_weight='balanced'`                 |
| Train/Test Split       | 80% / 20%, stratified                       |

---

## 📈 Results

| Metric              | Score      |
|----------------------|------------|
| **Accuracy**         | 98.2%      |
| **Precision (Spam)** | 0.94       |
| **Recall (Spam)**    | 0.92       |
| **F1-score (Spam)**  | 0.93       |

**Confusion Matrix:**

<p align="center">
  <img src="confusion_matrix.png" width="420" alt="Confusion Matrix">
</p>

---

## 🗂️ Project Structure

```
spam-detection-svm/
│
├── spam_classifier_svm.py     # Main Python script (train + evaluate + predict)
├── spam_classifier_svm.ipynb  # Google Colab notebook version
├── spam_mail.csv              # Dataset (Category, Masseges)
├── confusion_matrix.png       # Saved confusion matrix plot
├── requirements.txt           # Python dependencies
└── README.md                  # Project documentation
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
```

Install dependencies:

```bash
pip install -r requirements.txt
```

**requirements.txt**
```
pandas
scikit-learn
matplotlib
seaborn
```

---

## ▶️ Usage

### Run locally
```bash
python spam_classifier_svm.py
```
You'll see the model's accuracy/classification report printed, followed by an interactive prompt where you can type any message and instantly get a prediction.

### Run on Google Colab
Click the badge below to open and run the notebook directly in your browser — no local setup required:

<p align="center">
  <a href="https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/spam_classifier_svm.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">
  </a>
</p>

> ⚠️ In Colab, upload `spam_mail.csv` via the file browser (or mount Google Drive) before running the notebook.

---

## 🛠️ Tech Stack

- **Python 3.9+**
- **Pandas** – data handling
- **Scikit-learn** – TF-IDF, SVM, evaluation metrics
- **Matplotlib / Seaborn** – visualization

---

## 🚀 Future Improvements

- [ ] Compare SVM with Naive Bayes, Logistic Regression, and Random Forest
- [ ] Add hyperparameter tuning with `GridSearchCV`
- [ ] Deploy as a web app using Streamlit or Flask
- [ ] Add support for HTML email parsing
- [ ] Experiment with word embeddings (Word2Vec / BERT) instead of TF-IDF

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to check the [issues page](https://github.com/YOUR_USERNAME/YOUR_REPO/issues) or submit a pull request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## ⭐ Show Your Support

If you found this project helpful, please consider giving it a ⭐ on GitHub — it helps others discover it too!

<p align="center">Made with ❤️ and a bit of Machine Learning</p>
