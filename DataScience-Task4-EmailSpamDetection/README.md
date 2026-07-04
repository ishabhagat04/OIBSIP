# Task 4: Email Spam Detection with Machine Learning

## Objective
Build a Natural Language Processing (NLP) binary classifier that distinguishes spam emails from legitimate (ham) emails.

## Dataset
- Source: Email Spam Dataset (`emails.csv`)
- Features: text (email content), spam (label: 1 = spam, 0 = ham)
- Total records: 5,728 emails

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn (TF-IDF, Multinomial Naive Bayes, Logistic Regression, SVM)
- NLTK / re (text preprocessing)
- Matplotlib, Seaborn
- WordCloud
- Google Colab

## Key Observations

### 1. Data Overview & Class Distribution
- **Ham (legitimate)**: 4,360 emails (76.12%)
- **Spam**: 1,368 emails (23.88%)
- The dataset is imbalanced (more ham than spam)

### 2. Text Preprocessing Pipeline
1. **Lowercase conversion**: Convert all text to lowercase for consistency
2. **Punctuation removal**: Remove special characters and punctuation marks
3. **Stopword removal**: Remove common words (e.g., "the", "is", "at", "which")
4. **Stemming**: Reduce words to their root form (e.g., "running" → "run", "played" → "play")

### 3. Feature Extraction: TF-IDF Vectorizer

**What is TF-IDF?**
TF-IDF (Term Frequency - Inverse Document Frequency) is a numerical statistic that reflects how important a word is to a document in a collection:

- **Term Frequency (TF)**: How often a word appears in a document
  - TF = (Number of times word appears in document) / (Total words in document)

- **Inverse Document Frequency (IDF)**: How rare or common a word is across all documents
  - IDF = log(Total documents / Number of documents containing the word)

- **TF-IDF = TF × IDF**
  - Words that appear frequently in one document but rarely in others get higher scores
  - Common words like "the" get very low scores
  - This helps identify words that are distinctive to spam emails

### 4. Model Performance Comparison

| Model | Accuracy | Precision | Recall | F1-Score |
|:---|:---|:---|:---|:---|
| Multinomial Naive Bayes | 98.69% | 97.58% | 97.24% | 97.41% |
| Logistic Regression | 97.91% | 98.54% | 93.10% | 95.74% |
| Support Vector Machine (SVM) | 98.95% | 98.94% | 96.90% | 97.91% |

**Best Model**: Support Vector Machine (SVM) with F1-Score of 97.91%

### 5. Why Recall is Important for Spam Detection

**Recall** measures the ability to correctly identify spam emails:
- Formula: **Recall = TP / (TP + FN)**
  - TP = True Positives (spam correctly identified)
  - FN = False Negatives (spam incorrectly classified as ham)

**Why Recall is prioritized:**
1. **False Negatives are more harmful**: A spam email reaching the user's inbox could contain phishing links, malware, or scams
2. **False Positives are less harmful**: A legitimate email going to spam is inconvenient but not dangerous
3. **User safety**: High recall ensures maximum spam protection
4. **Trust**: Users trust spam filters that catch most spam emails

**In short**: It's better to accidentally mark a ham email as spam (False Positive) than to let a spam email reach the user's inbox (False Negative).

### 6. Top Words Indicating Spam vs Ham

**Top Spam Words**: "medic", "free", "software", "http", "love", "life", "click", "remove", "subject", "survey", "ebay", "viagra", "guide", "win"

**Top Ham Words**: "enron", "vincent", "energy", "thank", "research", "password", "update", "kaminski", "attach", "houston", "model", "pdf", "risk", "option", "article"

### 7. Spam vs Ham WordCloud Insights

- **Common Spam Words**: "free", "win", "cash", "prize", "urgent", "click", "claim", "offer", "limited", "guaranteed"
- **Common Ham Words**: "hi", "hello", "love", "thanks", "good", "great", "sure", "see", "tonight", "call"

## How to Run

1. Open the notebook in Google Colab:
   - Go to [Google Colab](https://colab.research.google.com/)
   - Click on **File** → **Upload Notebook**
   - Upload `Task4_Email_Spam_Detection.ipynb`

2. Or open it directly from GitHub:
   - Go to your GitHub repository
   - Click on `Task4_Email_Spam_Detection.ipynb`
   - Click the **"Open in Colab"** button

3. Upload the dataset:
   - The notebook will prompt you to upload `emails.csv`
   - Download the dataset from Kaggle or other sources

4. Run all cells:
   - Click **Runtime** → **Run all**

## Files Included
- `Task4_Email_Spam_Detection.ipynb` - Main Jupyter Notebook with complete analysis
- `README.md` - Project documentation

## Results Summary
- ✅ Data loading and class distribution check completed
- ✅ Text preprocessing pipeline implemented (lowercasing, punctuation removal, stopword removal, stemming)
- ✅ TF-IDF feature extraction with detailed explanation
- ✅ Train/test split completed
- ✅ 3 classifiers trained (Multinomial Naive Bayes, Logistic Regression, SVM)
- ✅ Models evaluated using accuracy, precision, recall, F1-score, confusion matrix
- ✅ Recall importance discussion included
- ✅ Top spam/ham word identification
- ✅ WordCloud visualizations for spam and ham words (bonus)
- ✅ Clean, well-commented Jupyter Notebook