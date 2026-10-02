# Customer Incident Intelligence

> **An end-to-end NLP analytics platform for discovering recurring customer issues, understanding sentiment, and monitoring changes over time.**

**Portfolio project for data science / analytics students**

Customer Incident Intelligence turns unstructured customer complaints, reviews, and support tickets into an inspectable analytics workflow. The system is designed to work with **new datasets without requiring the user to manually map columns or define issue categories first**.

```text
CSV / XLSX / XLSM / XLS
        |
        v
Automatic schema detection
(text / date / evaluation fields)
        |
        v
Text cleaning + validation
        |
        v
MiniLM sentence embeddings
384-dimensional semantic vectors
        |
        v
Adaptive unsupervised clustering
        |
        +--------------------+
        |                    |
        v                    v
Issue discovery       Sentiment analysis
                      RoBERTa 3-class
        |                    |
        +---------+----------+
                  |
                  v
        Date-aware analytics
          (when dates exist)
                  |
          baseline comparison
          + lift + z-score
                  |
                  v
             Surge alerts
                  |
                  v
        FastAPI + Web Dashboard
