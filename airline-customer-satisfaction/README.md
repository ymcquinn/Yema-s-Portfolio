# ✈️ How Can Airlines Improve Customer Experience?
## Predicting Flight Recommendations with Machine Learning

### 📊 Overview
Built a classification model with **94% accuracy** to predict whether customers would recommend a flight, identifying key drivers of customer satisfaction through K-means clustering.

### 🎯 Business Problem
Airlines receive thousands of reviews but struggle to prioritize improvements. Which factors actually drive recommendations? Where should airlines invest limited resources for maximum impact?

### 📁 Dataset
- **Source**: Airline reviews dataset (provided by York University)
- **Time Period**: March 2016 - March 2024
- **Features**: Seat comfort, inflight entertainment, value for money, staff service, food & beverages, verified reviewer status, traveler type, route

### 🛠️ Methods

| Step | Technique | Purpose |
|------|-----------|---------|
| 1 | Data Cleaning & Preprocessing | Handle missing values, encode categorical variables |
| 2 | Feature Scaling | StandardScaler for numeric features |
| 3 | K-Means Clustering | Identify customer segments based on satisfaction patterns |
| 4 | Logistic Regression | Predict recommendation (Recommended = 1/0) |
| 5 | Model Evaluation | Classification report, accuracy, precision, recall |

### 🔍 Key Findings

**Customer Segments Identified:**
- **Cluster 0 (Highly Satisfied)**: Rated all features positively - focus on retention
- **Cluster 1 (Moderately Satisfied)**: Some dissatisfaction with inflight entertainment
- **Cluster 2 (Dissatisfied)**: Critical of value for money and food & beverages

**Top Predictors of Recommendations:**
1. Verified reviewer status (authenticity matters!)
2. Overall satisfaction
3. Value for money
4. Staff service

### 💡 Recommendations

| Priority | Action | Target Segment |
|----------|--------|----------------|
| 1 | Strengthen review verification process | All customers (improves data quality) |
| 2 | Improve inflight entertainment offerings | Clusters 1 & 2 |
| 3 | Re-evaluate pricing strategy on underperforming routes | Cluster 2 |
| 4 | Maintain high standards for highly satisfied customers | Cluster 0 |

### 📈 Impact
This analysis enables airlines to move from "what do customers complain about?" to "what improvements will actually increase recommendations?" - a data-driven approach to resource allocation.

### 🧰 Code & Tools
- **Language**: Python
- **Libraries**: pandas, scikit-learn, matplotlib, seaborn
- **Notebook**: [`airline_analysis.ipynb`](airline_analysis.ipynb)

### 📊 Visualizations
*(Add screenshots of your figures here once you upload them!)*

- Figure 1: Feature importance rankings
- Figure 2: Cluster profiles (average satisfaction scores by cluster)
- Confusion matrix showing model performance

### 📚 References
See full report for complete list of academic sources.

---

*Note: This project uses a dataset provided for academic purposes. Analysis and recommendations are original.*
