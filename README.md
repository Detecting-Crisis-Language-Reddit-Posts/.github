# Detecting Crisis Language in Reddit Posts

⚠️ _Update the above title with your AI Studio Challenge Project name. Remove all guidance notes and examples in this template before finalizing your README._

---

### 👥 **Team Members**

| Name             | GitHub Handle | Contribution                                                             |
|------------------|---------------|--------------------------------------------------------------------------|
| Sophia Lee       | @taylornguyen | Data Acquisition, Labeling, Exploratory Data Analysis (EDA), Logistic Regression, XGBoost and BERT Modeling|
| Adrija Rambhatla   | @Adrija0819 | Data Labeling, BERT Modeling, Exploratory Data Analysis (EDA)            |
| Amina Hassan     | @aminahassan  | Data preprocessing, feature engineering, data validation                 |
| Priya Mehta      | @pmehta       | Model selection, hyperparameter tuning, model training and optimization  |
| Chris Park       | @chrispark    | Model evaluation, performance analysis, results interpretation           |

---

## 🎯 **Project Highlights**

Built machine learning models to detect crisis-related mental health language in Reddit posts.
Fine-tuned a BERT-based classifier that achieved high recall for crisis posts, prioritizing safety-critical detection.
Compared traditional ML models (Logistic Regression, XGBoost) with transformer-based approaches.
Generated insights to support early intervention strategies for mental health organizations.
Balanced performance with ethical considerations such as false negatives and fairness.

---

## 👩🏽‍💻 **Setup and Installation**

**Provide step-by-step instructions so someone else can run your code and reproduce your results. Depending on your setup, include:**

* How to clone the repository
* How to install dependencies
* How to set up the environment
* How to access the dataset(s)
* How to run the notebook or scripts

---

## 🏗️ **Project Overview**

**Describe:**
This project was developed as part of the Break Through Tech AI Program – AI Studio, in collaboration with Abt Global, a research and consulting company focused on data-driven social impact.
The objective of this project was to build a machine learning model capable of detecting mental health crisis language in Reddit posts. Early identification of crisis signals can enable faster, more effective intervention and resource allocation.
Mental health crises are often first expressed online. Automating the detection of high-risk language has the potential to:
Support moderators and crisis response teams
Reduce time to intervention
Improve outcomes for individuals in distress
---

## 📊 **Data Exploration**

**You might consider describing the following (as applicable):**
Data Source: Reddit posts from r/depression subreddit
Data Type: Text data, numerical features
Size: ~135k posts and comments
Format: CSV files containing post text and labels


Preprocessing Steps
Text cleaning (lowercasing, punctuation removal, removed non-english words)
Tokenization
Stopword removal (for traditional ML models)
Class imbalance handling via weighting


EDA Insights
Sentiment Analysis
Strong class imbalance required recall-focused evaluation
Keywords alone were insufficient—context was critical


**Potential visualizations to include:**

* Plots, charts, heatmaps, feature visualizations, sample dataset images

---

## 🧠 **Model Development**

**You might consider describing the following (as applicable):**
Models Implemented
Logistic Regression (TF-IDF features)
XGBoost
BERT (fine-tuned transformer model)
Training Setup
80% training and validation / 20% test split
Primary metric: Recall for crisis class
Secondary metrics: Precision, F1-score
Hyperparameter Tuning
Grid search for traditional models
Learning rate and epoch tuning for BERT



---

## 📈 **Results & Key Findings**

Insert table comparing all 4 models

Key Findings
BERT significantly outperformed traditional models in capturing contextual crisis language.
Emphasizing recall reduced false negatives, aligning with real-world safety needs.
Some demographic and linguistic bias risks were identified, highlighting the need for careful deployment.
---

## 🚀 **Next Steps**

Expand training data to include more diverse communities and language styles.
Explore domain-adapted transformers (e.g., mental-health–specific BERT variants).
Conduct deeper fairness and bias audits.
Investigate explainability tools to improve model transparency.

---

## 📝 **License**

If applicable, indicate how your project can be used by others by specifying and linking to an open source license type (e.g., MIT, Apache 2.0). Make sure your Challenge Advisor approves of the selected license type.

**Example:**
This project is licensed under the MIT License.

---

## 📄 **References** (Optional but encouraged)

CITE papers, documentations, etc.

## 🙏 **Acknowledgements** (Optional but encouraged)

We would like to thank Manav Desai, our AI Studio coach, for his immense support and patience throughout our project development and modeling process. We would also like to thank our challenge advisors, Zachary Allen, Anita Nti, and Dr. Nikki, for their valuable feedback and critiques, which helped us grow.


---

## 🙏 **Acknowledgements** (Optional but encouraged)

Thank your Challenge Advisor, host company representatives, TA, and others who supported your project.
