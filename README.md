# Big Data Analytics on Yelp Dataset

## 📌 Overview

This project presents a comprehensive Big Data pipeline built using PySpark to analyze and extract insights from the [Yelp Open Dataset](https://business.yelp.com/data/resources/open-dataset/). The work spans data preprocessing, exploratory analysis, graph analytics, recommendation systems, and sentiment/topic modeling.

## 👨‍💻 Team

- Maysam Khatib
- Panagiotis Michael
- Fivos Theodoridis

## 📁 Project Structure

```bash
.
├── Preprocessing_EDA.pdf
├── Review_Tip_EDA.pdf
├── graph_analysis_setup_and_plot.pdf
├── graphs_setup_plot_algorithms.pdf
├── recommendation_system.pdf
├── text_analysis_topic_detection_ml.pdf
├── Yelp Dataset Documentation & ToS copy.pdf
├── dataset_source.txt
├── README.md
```

## 📦 Dataset

The project uses the [Yelp Open Dataset](https://business.yelp.com/data/resources/open-dataset/) containing JSON files related to businesses, users, reviews, tips, and check-ins. Refer to the [official documentation](https://github.com/Yelp/dataset-examples) for format details.

---

## ⚙️ Environment Setup

Install required packages:
```bash
pip install pyspark
pip install graphframes
pip install basemap
pip install nltk
pip install textblob
```

Ensure Spark is properly configured with sufficient memory:
```python
SparkSession.builder \
    .appName("YelpEDA") \
    .config("spark.jars.packages", "graphframes:graphframes:0.8.2-spark3.1-s_2.12") \
    .config("spark.driver.memory", "32g") \
    .config("spark.executor.memory", "32g") \
    .getOrCreate()
```

---

## 🧹 1. Preprocessing & Exploratory Data Analysis (EDA)

Located in `Preprocessing_EDA.pdf`, this phase includes:
- Schema inspection of business and user datasets
- Filtering open businesses
- Basic visualizations using `matplotlib`, `seaborn`, and `basemap`

Refer to:
- `Review_Tip_EDA.pdf` for review and tip file analysis
- `text_analysis_topic_detection_ml.pdf` for sentiment classification preparation

---

## 🔗 2. Graph-Based Analysis

See `graph_analysis_setup_and_plot.pdf` and `graphs_setup_plot_algorithms.pdf`:
- Construct user–user friendship networks
- User–business bipartite graphs
- Business co-review networks
- GraphFrames and NetworkX used for analysis and visualization

---

## 🤖 3. Recommendation System

Refer to `recommendation_system.pdf`:
- Implemented Collaborative Filtering using ALS from `pyspark.ml.recommendation`
- Filtering for active users and businesses
- Evaluation using RMSE

---

## 🧠 4. Text Analytics & Machine Learning

As detailed in `text_analysis_topic_detection_ml.pdf`:
- Sentiment analysis by mapping review stars
- Topic modeling using LDA
- Feature extraction using CountVectorizer, TF-IDF
- Classification with Logistic Regression, SVM, and others

---

## 📊 Visualizations

Various plots are used to analyze:
- Business categories
- Star distributions
- Graph centrality
- Word clusters and topics

---

## ✅ License & Terms

Use of Yelp data is governed by [Yelp's Dataset Terms of Use](https://www.yelp.com/dataset/terms). See `Yelp Dataset Documentation & ToS copy.pdf` for details.

---

## 📬 Citation

If you use this work, please cite the original Yelp Dataset and acknowledge the authors of this project.
