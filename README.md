# 📩 SMS Spam Detection using Machine Learning

A Machine Learning project that classifies SMS messages as **Spam** or **Ham (Legitimate Message)** using Natural Language Processing (NLP) and several classification algorithms.

The project includes text preprocessing, feature extraction using TF-IDF, model training, and evaluation. It also includes a **Streamlit web application** that allows users to analyze SMS messages interactively.

## 📌 Project Overview

Spam messages are unwanted messages that may contain advertisements, suspicious links, or fraudulent content. This project aims to automatically identify spam messages and distinguish them from legitimate SMS messages using Machine Learning.

### 🎯 Objectives

* Build a text classification system for SMS messages.
* Apply NLP techniques to clean and preprocess text data.
* Convert text into numerical features using TF-IDF.
* Train and compare multiple Machine Learning classifiers.
* Build an interactive web application using Streamlit.

## 📊 Dataset

**Dataset:** SMS Spam Collection Dataset

The dataset contains SMS messages labeled as either spam or legitimate messages.

| Feature  | Description                   |
| -------- | ----------------------------- |
| `Target` | Message category: Spam or Ham |
| `Text`   | Original SMS message          |

**Dataset size:** 5,572 messages before preprocessing.

Duplicate rows were removed during data cleaning.

## ⚙️ Project Workflow

### 1. Data Cleaning

* Loaded and inspected the dataset.
* Renamed the columns to `Target` and `Text`.
* Removed duplicate rows.

### 2. Text Preprocessing (NLP)

The following preprocessing steps were applied:

* **Text Cleaning:** Removed non-alphabetic characters using Regular Expressions.
* **Lowercasing:** Converted text to lowercase.
* **Tokenization:** Split messages into individual words.
* **Stopword Removal:** Removed common words using NLTK.
* **Lemmatization:** Reduced words to their base forms.
* **Text Reconstruction:** Joined processed tokens into cleaned text.

### 3. Feature Extraction

Used **TF-IDF (Term Frequency–Inverse Document Frequency)** to transform the preprocessed SMS messages into numerical feature vectors suitable for Machine Learning models.

### 4. Model Training and Evaluation

Trained and compared six Machine Learning classification algorithms.

## 🤖 Models and Results

The models achieved the following accuracy scores in the project evaluation:

| Rank | Model                           | Accuracy |
| ---: | ------------------------------- | -------: |
|    1 | Random Forest Classifier        |   97.39% |
|    2 | Support Vector Classifier (SVC) |   96.81% |
|    3 | Multinomial Naive Bayes         |   96.23% |
|    4 | Logistic Regression             |   95.84% |
|    5 | Decision Tree Classifier        |   95.26% |
|    6 | K-Nearest Neighbors (KNN)       |   90.72% |

**Best-performing model:** Random Forest Classifier, with an accuracy of **97.39%** in the reported evaluation.

*Note: Accuracy results depend on the dataset split and evaluation procedure. Accuracy alone does not describe every aspect of a classifier's performance.*

## 🖥️ Streamlit Web Application

The project includes a Streamlit interface with the following sections:

* **Home & Analyzer:** Enter an SMS message and analyze its predicted category.
* **Model Performance:** View the model evaluation results.
* **About Project:** Read information about the project and its workflow.

The application uses the trained Random Forest model and the fitted TF-IDF vectorizer to process input messages and generate predictions.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* NLTK
* Regular Expressions (`re`)
* TF-IDF Vectorization
* Streamlit
* Plotly
* Google Colab
* Git & GitHub

## 📂 Project Structure

```text
SMS-Spam-Detection/
│
├── app.py                  # Streamlit web application
├── SMS_Spam_Detection.ipynb # Jupyter Notebook and ML workflow
├── requirements.txt        # Project dependencies
└── README.md               # Project documentation
```

*The exact filenames may differ depending on how the files are uploaded to the repository.*

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd SMS-Spam-Detection
```

Replace `<YOUR_GITHUB_REPOSITORY_URL>` with your repository URL.

### 2. Install Dependencies

It is recommended to use a virtual environment.

```bash
pip install -r requirements.txt
```

### 3. Run the Streamlit Application

```bash
streamlit run app.py
```

Open the local URL displayed in the terminal to use the application.

### ⚠️ Model Files

The application requires the trained model and fitted TF-IDF vectorizer files:

* `rf_model.pkl`
* `tfidf_vectorizer.pkl`

Make sure these files are available at the paths expected by `app.py` before running the application.

**Important:** Only load pickle files from trusted sources.

## 📈 Future Improvements

* Evaluate models using Precision, Recall, F1-score, and a Confusion Matrix.
* Analyze performance on unseen messages.
* Improve text preprocessing and feature engineering.
* Explore additional classification algorithms.
* Deploy the Streamlit application online.
* Improve the user interface and add more detailed prediction insights.

## 👨‍💻 Author

**Eslam Ahmed Hosny**

Computer & Control Systems Engineering Student
Machine Learning & AI Enthusiast

---

⭐ If you find this project useful, consider giving the repository a star!
