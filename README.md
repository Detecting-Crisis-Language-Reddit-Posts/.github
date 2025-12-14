# Detecting Crisis Language in Reddit Posts

---

### 👥 **Team Members**

| Name             | GitHub Handle | Contribution                                                             |
|------------------|---------------|--------------------------------------------------------------------------|
| Sophia Lee       | @taylornguyen | Data Acquisition, Labeling, Exploratory Data Analysis (EDA), Logistic Regression, XGBoost and BERT Modeling|
| Adrija Rambhatla | [@Adrija0819](https://github.com/Adrija0819) | Data Labeling, BERT Modeling, Exploratory Data Analysis (EDA)|
| Winnie Nna       | [@Winnie-Vallonia](https://github.com/Winnie-Vallonia) | Data Labeling, Exploratory Data Analysis (EDA), Model Evaluation and Comparison|
| Amina Hassan     | @aminahassan  | Data preprocessing, feature engineering, data validation                 |
| Priya Mehta      | @pmehta       | Model selection, hyperparameter tuning, model training and optimization  |
| Chris Park       | @chrispark    | Model evaluation, performance analysis, results interpretation           |

---

## 🎯 **Project Highlights**

* Built **machine learning models to detect crisis-related mental health language** in Reddit posts.
* Fine-tuned a **BERT-based classifier** that achieved high recall for crisis posts, prioritizing safety-critical detection.
* Compared traditional ML models (Logistic Regression, XGBoost) with transformer-based approaches.
* Generated insights to **support early intervention strategies** for mental health organizations.
* Balanced performance with **ethical considerations** such as false negatives and fairness.

---
## 📁 Project Structure

This project is hosted in Google Drive:  [Abt Global 2A](https://drive.google.com/drive/u/0/folders/12k9X6au9xDd4Oep5bRqfc_DdT0tcpRYA)

The project is organized as follows:

- **AbtGlobal2A.ipynb**  
  Main Google Colab notebook containing the end-to-end pipeline, including data loading, preprocessing, model training, and evaluation.

- **Reddit_Cleaning_Pipeline.ipynb**  
  Notebook used for scraping, cleaning, and preprocessing Reddit data prior to modeling.

- **Data/**  
  Raw and cleaned datasets used across all models.

- **Train/Val/Split Files/**  
  Preprocessed train, validation, and test splits used for model training and evaluation.

- **Feature Engineering/**  
  Scripts and notebooks related to text preprocessing and feature extraction.

- **Logistic Regression Model/**  
  Implementation and experiments for the logistic regression baseline.

- **XGBoost Model/**  
  Implementation and experiments for the XGBoost model.

- **RoBERTa Model/**  
  Fine-tuning and evaluation of the RoBERTa deep learning model.

- **Sentiment Analysis/**  
  Supporting analysis and experiments related to sentiment-based features.

- **Topic Modeling/**  
  Topic modeling experiments and analysis.

- **Model Evaluation/**  
  Evaluation scripts, metrics, and result visualizations.

- **Documentation/**  
  Project documentation and written explanations.

- **Presentations/**  
  Slides used for project presentations.



## 👩🏽‍💻 **Setup and Installation**

This project was developed and run entirely in Google Colab, so no local setup is required.
- **1. Access the notebook**

Open the provided Google Colab notebook using the shared link: [Google Colab notebook](https://colab.research.google.com/drive/1cdoSySG-F-7g1fmHArz-E6DXJRKNT65X)


- **2. Install dependencies**

All required libraries like NumPy, pandas, PyTorch, scikit-learn are installed directly within the notebook using pip.

- **3. Set up the environment**

The datasets are stored in Google Drive.
To access them, the notebook mounts Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```


- **4. Access the datasets**

After mounting, the data is accessed via the following path:
*/content/drive/MyDrive/Abt Global 2A/Data/

- **5. Run the notebook**

* Run all cells from top to bottom to reproduce the full pipeline, including:

* Data loading and preprocessing

* Model training

* Evaluation and results


---

## 🏗️ **Project Overview**

This project was developed as part of the Break Through Tech AI Program – AI Studio, in collaboration with Abt Global, a research and consulting company focused on data-driven social impact.
The objective of this project was to build a machine learning model capable of detecting mental health crisis language in Reddit posts. Early identification of crisis signals can enable faster, more effective intervention and resource allocation.
Mental health crises are often first expressed online. Automating the detection of high-risk language has the potential to:
* Support moderators and crisis response teams
* Reduce time to intervention
* Improve outcomes for individuals in distress
---

## 📊 **Data Exploration**

**Data Source:** Reddit posts from r/depression subreddit

**Data Type:** Text data, numerical features

**Size:** ~135k posts and comments

**Format:** CSV files containing post text and labels


**Preprocessing Steps:**
* Text cleaning (lowercasing, punctuation removal, removed non-english words)
* Tokenization
* Stopword removal (for traditional ML models)
* Class imbalance handling via weighting


**EDA Insights:**
* Sentiment Analysis
* Strong class imbalance required recall-focused evaluation
* Keywords alone were insufficient—context was critical


**Potential visualizations to include:**

* Plots, charts, heatmaps, feature visualizations, sample dataset images

### Word Cloud Visualization
<img width="790" alt="wordcloud" src="https://github.com/user-attachments/assets/c79cab13-3717-4de7-86ee-2b9013d00b70" />

*Figure 1: Word cloud of frequent terms in crisis-related Reddit posts.*

### Topic Modeling Results
<img width="979" alt="Topic Modeling Bar Chart" src="https://github.com/user-attachments/assets/fa4d8c06-e4f3-4da5-933d-35bb266c548c" />

*Figure 2: Distribution of topics identified through topic modeling.*

---

## 🧩 Code Highlights

- **Reddit_Cleaning_Pipeline.ipynb**  
  Cleans and preprocesses Reddit text data (e.g., normalization and filtering) and prepares datasets for modeling.

- **AbtGlobal2A.ipynb**  
  Main notebook containing the full ML pipeline, including feature engineering (e.g., TF-IDF for traditional models), model training (Logistic Regression, XGBoost, BERT, RoBERTa), and evaluation (precision, recall, F1-score, ROC-AUC) with visual comparisons.

- **Data/** and **Train/Val/Split Files/**  
  Stores raw/cleaned datasets and the preprocessed train/validation/test splits used by the notebooks.

---

## 🧠 **Model Development**

**Models Implemented:**
* Logistic Regression (TF-IDF features)
* XGBoost
* BERT (fine-tuned transformer model)

**Training Setup:**
* 80% training and validation / 20% test split
* Primary metric: Recall for crisis class
* Secondary metrics: Precision, F1-score

**Hyperparameter Tuning:**
* Grid search for traditional models
* Learning rate and epoch tuning for BERT

---

## 📈 **Results & Key Findings**

### Model Performance Comparison

<img width="886" height="493" alt="image" src="https://github.com/user-attachments/assets/95a82318-4972-4660-9cc7-48df8033344d" />

*Figure 3: Performance comparison of four models on the test set using weighted Precision, Recall, F1-score, and ROC-AUC.*

<img width="1227" height="562" alt="Screenshot 2025-12-14 at 6 15 28 PM" src="https://github.com/user-attachments/assets/a3ce61a3-b9d4-4bdb-b289-d61dd82dfe6c" />

*Figure 4: High-level comparison of model features, strengths, and weaknesses across Logistic Regression, XGBoost, BERT, and RoBERTa.*

### Quantitative Results

| Model                | Precision (Weighted) | Recall (Weighted) | F1-score (Weighted) | ROC-AUC |
|----------------------|----------------------|-------------------|---------------------|---------|
| Logistic Regression  | 0.82                 | 0.76              | 0.78                | 0.82    |
| XGBoost              | 0.78                 | 0.80              | 0.79                | 0.79    |
| BERT                 | 0.94                 | 0.94              | 0.94                | 0.98    |
| RoBERTa              | 0.52                 | 0.84              | 0.64                | 0.87    |


**Key Findings**
* BERT significantly outperformed traditional models in capturing contextual crisis language.
* Emphasizing recall reduced false negatives, aligning with real-world safety needs.
* Some demographic and linguistic bias risks were identified, highlighting the need for careful deployment.


---

## 💭 Discussion & Reflection

- **What worked:** BERT achieved the strongest and most balanced performance across metrics. Its contextual understanding helped capture nuanced crisis language beyond keywords (e.g., indirect expressions of distress).

- **Why baseline models struggled:** Logistic Regression and XGBoost relied heavily on surface-level patterns (e.g., TF-IDF/engineered features). This made them less effective at handling context, negation, and subtle phrasing, which are common in real crisis-related posts.

- **Why RoBERTa underperformed BERT:** Although RoBERTa is a more heavily optimized transformer, performance depends on fine-tuning setup and data characteristics. In our experiments, RoBERTa showed higher recall but much lower precision, suggesting it over-flagged posts as crisis-related (more false positives). This highlights that a more complex model does not automatically yield better real-world performance without careful tuning and calibration.

- **Takeaway:** Model selection should be driven by empirical results and task priorities (e.g., recall vs. precision), not just model complexity.

---

## 🚀 **Next Steps**

* Expand training data to include more diverse communities and language styles.
* Explore domain-adapted transformers (e.g., mental-health–specific BERT variants).
* Conduct deeper fairness and bias audits.
* Investigate explainability tools to improve model transparency.

---

## 📝 **License**

If applicable, indicate how your project can be used by others by specifying and linking to an open source license type (e.g., MIT, Apache 2.0). Make sure your Challenge Advisor approves of the selected license type.

**Example:**
This project is licensed under the MIT License.

---

## 📄 **References** 

[1] N. H. Kim, J. M. Kim, D. M. Park, S. R. Ji, and J. W. Kim, “Analysis of depression in social media texts through the Patient Health Questionnaire-9 and natural language processing,” *Digital Health*, vol. 8, Jul. 2022, Art. no. 20552076221114204. doi:10.1177/20552076221114204. https://pmc.ncbi.nlm.nih.gov/articles/PMC9297458/


---

## 🙏 **Acknowledgements**

We would like to thank Manav Desai, our AI Studio coach, for his immense support and patience throughout our project development and modeling process. We would also like to thank our challenge advisors, Zachary Allen, Anita Nti, and Dr. Nikki, for their valuable feedback and critiques, which helped us grow.
