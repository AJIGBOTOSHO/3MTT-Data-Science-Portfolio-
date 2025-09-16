# 🚫 Fake News Detection Using NLP & Machine Learning

> A binary classification system to detect fake news articles using text analysis, NLP techniques, and machine learning models — built as part of the 3MTT Data Science Course.

---

## 📌 Problem Statement

With the rapid spread of misinformation online, distinguishing between real and fake news has become critical. This project builds an automated classifier that analyzes article content to predict whether a news piece is **real** or **fake**, helping platforms, journalists, and readers make informed decisions.

---

## 📊 Dataset

- **Source**: [Kaggle: Fake News Dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)  
- **Size**: ~20,000 articles (10,000 real, 10,000 fake)  
- **Features**:  
  - `title`: Headline of the article  
  - `text`: Full body content  
  - `label`: `0` = Real, `1` = Fake  
- **Preprocessing**:  
  - Removed HTML tags, special characters, and stopwords  
  - Lowercased all text  
  - Combined `title` + `text` for richer context  

---

## 🛠️ Methodology

| Step | Technique |
|------|-----------|
| **Text Vectorization** | TF-IDF (Term Frequency-Inverse Document Frequency) |
| **Models Tested** | Logistic Regression and  Random Forest |
| **Evaluation Metrics** | Accuracy, Precision, Recall, F1-Score, ROC-AUC |
| **Best Model** | ✅ **Logistics Regression** |

### Why Logistic Regression Won:
- High accuracy with low complexity  
- Fast inference  
- Interpretable coefficients → we can see which words signal “fake” news  
- Outperformed deeper models due to limited data size and clean preprocessing

---

## 📈 Results

| Model | Accuracy | F1-Score | recall | precision | 
|-------|----------|----------|---------| ----------
| Logistic Regression | **91.7%** | **0.92** | **0.94** |   **0.94**  |
| Random Forest | 91.1% | **0.93** | **0.95** |  **0.91**| 

> 💡 **Key Insight**: Logistics models with strong feature engineering outperformed complex ones — proving that **clean data + good features matter more than model depth**.

---

## 🔍 Key Insights from EDA

- ✅ Fake news tends to use **emotional, sensational language** (“SHOCKING”, “YOU WON’T BELIEVE”)  
- ✅ Real news uses more **neutral, factual phrasing** and longer sentences  
- ✅ Words like *“exposed,” “truth,” “must watch,” “conspiracy”* strongly correlate with fake labels  
- ✅ Headlines are more predictive than full text — suggesting users are often misled by titles alone


---

## 🧰 Tech Stack

- Python 3.10  
- Pandas, NumPy  
- scikit-learn (`TfidfVectorizer`, `LogisticRegression`, `classification_report`)  
- NLTK, re (for text cleaning)  
- Matplotlib, Seaborn (for visualization)  
- Jupyter Notebook

---

## 🎯 Business Impact

This model can be integrated into:
- Social media platforms (e.g., Twitter/X, Facebook)  
- Browser extensions that flag suspicious headlines  
- News aggregation apps (Google News, Apple News)  
- Fact-checking tools used by journalists

Even at 92% accuracy, it reduces manual review workload by over 90%.

---

## 🙌 Acknowledgments
  
- 3MTT instructors and peers for feedback and support  
- The broader NLP community for foundational techniques

---

## 📄 License

MIT © 2025 [Hammed Olaitan AJIGBOTOSHO]

---
