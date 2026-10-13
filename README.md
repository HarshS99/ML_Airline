
# ✈️ Airline Customer Satisfaction Prediction

<p align="center">
  <b>An End-to-End Machine Learning Project for Predicting Airline Passenger Satisfaction</b>
  <br />
  Built with Python, LightGBM, Scikit-learn, and Streamlit
</p>

---

## 📌 Overview

The **Airline Customer Satisfaction Prediction App** is a machine learning-powered web application that predicts whether an airline passenger is **Satisfied** or **Neutral/Dissatisfied** based on their travel experience, service quality, and flight details.

The project uses the Kaggle Airline Passenger Satisfaction dataset, compares multiple classification algorithms, and selects **LightGBM** as the final model based on the project's evaluation results.

The trained model is integrated into an interactive Streamlit application, allowing users to enter passenger details and receive a satisfaction prediction.

## ✨ Key Features

- 🤖 **Machine Learning:** Implements seven classification algorithms.
- 🏆 **Model Selection:** Selects LightGBM based on evaluation performance.
- 📊 **Model Comparison:** Compares traditional ML algorithms with gradient boosting.
- 🧹 **Data Preprocessing:** Handles missing values, categorical encoding, and feature scaling where appropriate.
- 🎯 **Passenger Prediction:** Predicts satisfaction from flight and service-related information.
- 🌐 **Interactive UI:** Provides a user-friendly Streamlit interface.
- 💾 **Model Persistence:** Saves the trained model for reuse during inference.
- 🚀 **Deployment Ready:** Structured for deployment using Streamlit Community Cloud.

## 🧠 Machine Learning Workflow

```text
       Kaggle Dataset
              |
              ▼
     Data Preprocessing
              |
              ▼
   Exploratory Data Analysis
              |
              ▼
      Feature Engineering
              |
              ▼
       Train-Test Split
              |
              ▼
      Model Training
              |
              ▼
    Model Evaluation
              |
              ▼
      Model Selection
              |
              ▼
    Best Model: LightGBM
              |
              ▼
      Model Serialization
              |
              ▼
      Streamlit Web App
              |
              ▼
 Passenger Satisfaction Prediction
```

## 📂 Dataset

**Dataset:** Airline Passenger Satisfaction

**Source:** [Kaggle Dataset](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)

The dataset contains passenger demographics, travel information, flight details, and service ratings that can help explain customer satisfaction.

### Important Features

| Feature | Description |
|---|---|
| Age | Passenger's age |
| Customer Type | Type of airline customer |
| Type of Travel | Business or personal travel |
| Class | Travel class |
| Flight Distance | Distance covered by the flight |
| Departure Delay | Departure delay in minutes |
| Arrival Delay | Arrival delay in minutes |
| In-flight Wi-Fi Service | Passenger rating for Wi-Fi |
| Seat Comfort | Passenger rating for seat comfort |
| In-flight Entertainment | Entertainment service rating |
| Online Boarding | Online boarding experience |
| Baggage Handling | Baggage service rating |

**Target Variable:** `satisfaction`

- `satisfied` — Passenger is satisfied.
- `neutral or dissatisfied` — Passenger is neutral or dissatisfied.

*The features above are representative of the original dataset. The final application uses the features retained in its training pipeline.*

## 🤖 Models Implemented

Seven machine learning classification algorithms were evaluated.

| Algorithm | Approach |
|---|---|
| Logistic Regression | Linear classification |
| Decision Tree | Rule-based learning |
| Random Forest | Ensemble learning |
| K-Nearest Neighbors (KNN) | Distance-based classification |
| Support Vector Machine (SVM) | Maximum-margin classification |
| XGBoost | Gradient boosting |
| LightGBM | Gradient boosting with efficient tree learning |

### 🏆 Best Model: LightGBM

LightGBM was selected as the final model based on the evaluation results obtained during experimentation.

**Why LightGBM?**

- Efficient training on structured tabular data.
- Ability to learn nonlinear patterns.
- Support for complex feature interactions.
- Effective gradient-boosting approach for classification tasks.

### 📈 Evaluation Metrics

The models can be evaluated using:

- **Accuracy:** Overall proportion of correct predictions.
- **Precision:** Proportion of positive predictions that are correct.
- **Recall:** Proportion of actual positive cases correctly identified.
- **F1-Score:** Harmonic mean of precision and recall.
- **Confusion Matrix:** Breakdown of correct and incorrect classifications.

> Actual accuracy and other metric values should be added from the model evaluation results rather than estimated.

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Language | Python |
| Web Framework | Streamlit |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Boosting Algorithms | LightGBM, XGBoost |
| Model Persistence | Pickle / Joblib |
| Dataset | Kaggle |

## 📁 Project Structure

```text
airline-customer-satisfaction/
│
├── app.py
├── train_model.py
├── requirements.txt
├── README.md
│
├── data/
│   └── airline_passenger_satisfaction.csv
│
└── model_artifacts/
    └── best_model.pkl
```

*Update the structure to match your actual repository files.*

## ⚙️ Installation and Setup

### Prerequisites

- Python 3.10 or a compatible version
- pip
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/airline-customer-satisfaction.git
cd airline-customer-satisfaction
```

Replace `YOUR_USERNAME` and the repository name with your actual GitHub details.

### 2. Create a Virtual Environment

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows**

```bash
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Prepare the Dataset

Download the dataset from Kaggle and place the CSV in the `data/` directory.

Ensure the dataset filename and target column match the training script.

### 5. Train the Model

```bash
python train_model.py
```

This step trains and evaluates the models and saves the selected model artifact, assuming the training script is configured accordingly.

### 6. Launch the Streamlit Application

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal, typically:

`http://localhost:8501`

## 🌐 Deployment

The application can be deployed using [Streamlit Community Cloud](https://streamlit.io/cloud).

1. Push the project to GitHub.
2. Include `app.py`, `requirements.txt`, and the required model artifact.
3. Connect your GitHub repository to Streamlit Community Cloud.
4. Select `app.py` as the entry point.
5. Deploy and test the application.

Ensure that the deployed environment uses compatible versions of the libraries used during model training.

## 🔮 Future Enhancements

- [ ] Add an interactive model comparison dashboard.
- [ ] Visualize feature importance.
- [ ] Integrate SHAP for explainable AI.
- [ ] Display prediction probabilities where supported.
- [ ] Add cross-validation and hyperparameter tuning.
- [ ] Add automated tests for preprocessing and inference.
- [ ] Improve UI with interactive charts and a responsive layout.
- [ ] Publish a live application demo.

## 🎓 Key Learnings

This project demonstrates practical experience with:

- End-to-end machine learning workflows.
- Data cleaning and preprocessing.
- Feature encoding and transformation.
- Classification algorithms and ensemble learning.
- Model evaluation and selection.
- Saving and loading trained ML models.
- Deploying machine learning applications using Streamlit.

## 👨‍💻 Author

**Harsh Singh**

B.Tech Computer Science Engineering | AI/ML Developer

- **GitHub:** [HarshS99](https://github.com/HarshS99)
- **LinkedIn:** [Harsh Singh](https://www.linkedin.com/in/harsh-singh-b49020301/)

## ⭐ Show Your Support

If you find this project interesting, consider giving the repository a ⭐ on GitHub!

---

<p align="center">
  <b>Built with Python, Machine Learning, and Streamlit ❤️</b>
</p>
