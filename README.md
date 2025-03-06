# 📊 Amazon Reviews Analysis using BERTopic and Machine Learning

## 📌 Introduction
This project aims to analyze **Amazon reviews** related to **musical instruments** using **BERTopic** for topic modeling and various machine learning models for rank prediction. The study explores how different product features and review content influence **product rankings on Amazon**.

## 📂 Project Structure

## 📊 Dataset
The dataset is sourced from **Jianmo Ni (2018)**, containing **Amazon reviews and metadata**. This study focuses on **musical instruments**, analyzing how review content correlates with product rankings.

### 🎼 Data Statistics
| Product Category              | Review Count | Reviewer Count | Product Count |
|--------------------------------|--------------|---------------|--------------|
| Guitars & Basses              | 77,484       | 70,481        | 11,377       |
| Percussion Instruments        | 68,475       | 61,227        | 8,611        |
| Keyboards & Electronic Music  | 81,431       | 79,336        | 5,835        |
| Orchestral Instruments        | 73,503       | 68,027        | 6,124        |
| Amplifiers & Effects          | 281,902      | 48,124        | 5,374        |
| Live & Recording Equipment    | 229,381      | 193,737       | 16,973       |
| Microphones & Accessories     | 138,337      | 122,405       | 6,630        |
| Other Instruments & Accessories | 553,504     | 391,540       | 45,509       |

## 🤖 BERTopic Analysis
We used **BERTopic** to extract latent themes from reviews. Below are the **top words** in each topic:

| Topic 1  | Topic 2  | Topic 3  | Topic 4  |
|----------|---------|---------|---------|
| mic      | guitar  | price   | works   |
| sound    | stand   | great   | works great |
| headphones | guitar stand | product | great |

## 📉 Regression Analysis
We examined the relationship between **product ranking** and various review features:

| Variable         | Coefficient | Std. Error | t-value | p-value | Significance |
|----------------|------------|------------|--------|--------|-------------|
| Intercept      | 16.1092    | 0.275      | 58.56  | 0      | ***         |
| Average Rating | -2.7167    | 0.062      | -43.78 | 0      | ***         |
| Price          | 0.0029     | 0          | 9.919  | 0      | ***         |
| Sentiment Score | 0.0931    | 0.028      | 3.343  | 0.001  | **          |

## 🔍 Machine Learning Model Comparison
| Model                 | MSE (No Topic) | RMSE (No Topic) | R² (No Topic) | MSE (With Topic) | RMSE (With Topic) | R² (With Topic) |
|----------------------|--------------|--------------|------------|--------------|--------------|------------|
| Linear Regression   | 0.7398       | 0.8601       | 0.2819     | 0.7366       | 0.8582       | 0.2850     |
| Random Forest       | 0.2252       | 0.4745       | 0.7814     | 0.1067       | 0.3267       | 0.8964     |
| XGB Regressor      | 0.2049       | 0.4527       | 0.8011     | 0.1282       | 0.3580       | 0.8756     |

## 🎯 Conclusion
- **BERTopic-enhanced features improve model performance**, particularly in **Random Forest** and **XGBoost**.
- **Sentiment scores and review topics are crucial in ranking prediction**.

---

### 🚀 Future Work
- Expand dataset to include more product categories.
- Improve BERTopic model for better topic coherence.
- Explore **deep learning-based NLP models** like **BERT and Transformer-based architectures**.

📌 **For full implementation details, check the source code in this repository!**

---
**Author:** Hsien cheng Wu  

**Contact:** a0938528939@gmail.com

**License:** MIT
