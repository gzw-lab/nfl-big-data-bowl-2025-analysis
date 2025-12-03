# NFL Big Data Bowl 2025: Bayesian Player Rating System

### 🏆 Project Overview
This project was developed for the [Kaggle NFL Big Data Bowl 2025](https://www.kaggle.com/competitions/nfl-big-data-bowl-2025), focusing on pre-snap player behavior to predict post-snap outcomes. 

**Objective:** Quantify player influence on play success using tracking data.
**Role:** Machine Learning Engineer / Researcher
**Tools:** AWS (EMR, S3), PySpark, Python (Pandas, Scikit-learn), Parquet.

---

### 🚀 Technical Architecture

#### 1. Data Engineering (Big Data Pipeline)
* **Ingestion:** Processed terabytes of Next Gen Stats (NGS) tracking data (10 Hz location feeds) stored in **AWS S3**.
* **Optimization:** Converted raw CSV logs into partitioned **Parquet** files to optimize columnar storage.
* **Querying:** Leveraged **PySpark** for distributed processing, reducing feature extraction time by **25%** compared to standard Pandas workflows.
* **Feature Engineering:** Calculated lagged metrics (acceleration, jerk) and "snap-to-action" latency for 22 players per frame.

#### 2. Modeling Strategy (Bayesian & Regression)
* **Player Ratings:** Implemented a **Bayesian Hierarchical Model** to isolate individual player contribution from team performance noise. This allowed for robust ratings even for players with fewer snaps (shrinkage estimators).
* **Outcome Prediction:** Trained a **Logistic Regression** baseline and an **XGBoost** regressor to predict play success (EPA - Expected Points Added) based on pre-snap formation features.
* **Accuracy:** Achieved a predictive model accuracy of **87%** on the validation set.

---

### 📊 Key Results
* **Infrastructure:** Reduced end-to-end data processing latency by 25% through optimized PySpark queries.
* **Insights:** Identified that "defensive pre-snap motion" was a statistically significant predictor of run-stuff success rates.
* **Outcome:** System successfully rated 1,500+ players, providing a granular "Value Over Replacement" metric for defensive backs.

---

### ⚠️ Code Availability
*The full source code for this project is currently in a private repository due to ongoing updates and competition data usage agreements. Selected snippets or architectural diagrams can be provided upon request during an interview.*
