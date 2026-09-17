<div align="center">

# 🚆 RailPredict

### Machine Learning-Based Train Journey Time Prediction System

**Transforming railway journey data into intelligent duration predictions**

<br>

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Linear%20Regression-F7931E?style=for-the-badge)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Processing-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-Visualization-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)

<br>

**An end-to-end Machine Learning project developed as part of my  
Machine Learning Internship at Sysslan IT Solutions.**

</div>

---

## 🌟 About RailPredict

**RailPredict** is an end-to-end Machine Learning system designed to predict the **total duration of a train journey** using important journey characteristics.

The prediction is primarily based on:

- 📏 **Total Distance**
- 🚉 **Number of Stops**

The complete prediction flow is:

```text
Total Distance + Number of Stops
              ↓
      Linear Regression
              ↓
 Predicted Journey Duration
```

The project covers the complete Machine Learning lifecycle:

**Data Understanding → Data Cleaning → Feature Engineering → Exploratory Data Analysis → Model Training → Evaluation → Model Comparison → Interactive Application**

---

## 🎯 Project Objective

The main objective of RailPredict is to build a Machine Learning system capable of estimating the duration of a complete train journey from its distance and number of stops.

### 📥 Input Features

| Feature | Description |
|---|---|
| 📏 `Total_Distance` | Total distance of the train journey |
| 🚉 `Number_of_Stops` | Number of stops in the journey |

### 🎯 Target Variable

```text
Journey_Duration_Minutes
```

---

# 🏠 Journey Duration Prediction

The **Home page** contains the main Machine Learning prediction system.

Users enter:

- Total journey distance
- Number of stops

RailPredict then uses the trained Linear Regression model to estimate the **total journey duration**.

![RailPredict Home Page](screenshots/RailPredict_Homepage.png)

---

# 🗺️ Route Explorer

RailPredict also contains a dedicated **Route Explorer** for exploring train routes between stations.

Users can:

- 🚉 Select a starting station
- 📍 Select a valid destination
- 🚆 View trains operating between the stations
- 🛤️ Explore the station sequence
- 🕐 View arrival and departure information
- 📏 Calculate route distance
- 🔢 View the number of stops

![RailPredict Route Explorer](screenshots/Route_Page.png)

> **Note:** Route Explorer provides station-to-station route information. The Machine Learning model itself predicts the duration of a complete train journey.

---

# 📊 Interactive Analytics

The **Analytics dashboard** provides visual exploration of the train journey dataset.

It helps understand relationships between important journey characteristics such as:

- Distance
- Journey duration
- Number of stops
- Train journey patterns
- Dataset distributions

![RailPredict Analytics](screenshots/Train_Analytics.png)

---

# 💡 Data Insights

The **Insights page** summarizes important observations derived from the processed train journey dataset and Machine Learning analysis.

It provides an easier way to understand important characteristics of the data without manually examining the complete dataset.

![RailPredict Insights](screenshots/Train_Insights.png)

---

# 🧠 Machine Learning Model

## ⚙️ Algorithm Used

RailPredict uses:

### **Linear Regression**

The model learns the relationship between the input features and the journey duration.

```text
📏 Total Distance
        +
🚉 Number of Stops
        ↓
🤖 Linear Regression
        ↓
⏱️ Journey Duration
```

---

## 🧪 Train/Test Split

The Machine Learning dataset was divided into:

```text
80% → Training Data
20% → Testing Data
```

The training data was used to train the model, while the testing data was used to evaluate its performance on unseen records.

---

# 📈 Model Performance

The final **Distance + Stops Linear Regression model** achieved approximately:

| 📊 Metric | 🎯 Result |
|---|---:|
| **MAE** | **58.73 minutes** |
| **RMSE** | **157.58 minutes** |
| **R² Score** | **0.945** |

### 📌 Understanding the Metrics

**MAE — Mean Absolute Error**

The model's predictions differ from the actual journey durations by approximately **58.73 minutes on average**.

**RMSE — Root Mean Squared Error**

RMSE gives greater importance to larger prediction errors. The final model achieved an RMSE of approximately **157.58 minutes**.

**R² Score**

The model achieved an R² score of approximately **0.945**, indicating that the selected features explain a large proportion of the variation in journey duration within this dataset.

---

# ⚖️ Model Comparison

Two Linear Regression configurations were trained and compared.

### 🔹 Model 1 — Distance Only

```text
Total Distance
      ↓
Linear Regression
      ↓
Journey Duration
```

### 🔹 Model 2 — Distance + Stops

```text
Total Distance + Number of Stops
              ↓
      Linear Regression
              ↓
       Journey Duration
```

### 📊 Comparison Results

| Model | Features | MAE ↓ | RMSE ↓ |
|---|---|---:|---:|
| Model 1 | Distance Only | 67.51 | 167.48 |
| **Model 2** | **Distance + Stops** | **58.73** | **157.58** |

The **Distance + Stops model** achieved lower MAE and RMSE than the Distance Only model.

Therefore, the **Distance + Stops Linear Regression model was selected as the final model** for journey duration prediction.

![RailPredict Model Comparison](screenshots/Model_Comparision.png)

---

# 🔬 Project Development Workflow

The internship project was completed through **six levels**.

```text
📂 Raw Railway Dataset
          ↓
🔍 Level 1 — Data Understanding
          ↓
🧹 Level 2 — Data Cleaning & Feature Engineering
          ↓
📊 Level 3 — Exploratory Data Analysis
          ↓
🧠 Level 4 — Model Training & Evaluation
          ↓
⚖️ Level 5 — Model Comparison
          ↓
🖥️ Level 6 — Interactive ML System
          ↓
🚆 RailPredict
```

---

## 🔍 Level 1 — Data Understanding

The first stage focused on understanding the structure and quality of the train dataset.

Tasks included:

- Inspecting dataset size and columns
- Understanding data types
- Identifying train-wise starting and ending stations
- Calculating distance and stop statistics
- Checking missing values
- Checking duplicate records
- Identifying incorrect or inconsistent values

---

## 🧹 Level 2 — Data Cleaning & Feature Engineering

The raw station-level train data was cleaned and transformed into a train-level Machine Learning dataset.

Important features were created:

```text
Total_Distance
Number_of_Stops
Journey_Duration_Minutes
```

Arrival and departure information was processed to calculate the complete journey duration for individual trains.

---

## 📊 Level 3 — Exploratory Data Analysis

Exploratory Data Analysis was performed to understand relationships within the train journey data.

The analysis included:

- 📏 Distance vs Journey Duration
- 🚉 Number of Stops vs Journey Duration
- 🔥 Correlation analysis
- 📊 Train-wise stop analysis
- 📋 Pivot-table based exploration

---

## 🧠 Level 4 — Model Training & Evaluation

The processed train-level dataset was divided into training and testing sets.

A **Linear Regression** model was trained using:

```python
X = ["Total_Distance", "Number_of_Stops"]
y = "Journey_Duration_Minutes"
```

The model was evaluated using:

- MAE
- RMSE
- R² Score
- Actual vs Predicted visualization

---

## ⚖️ Level 5 — Model Comparison

Two different feature configurations were compared:

```text
Model 1 → Distance Only

Model 2 → Distance + Stops
```

The second model achieved lower prediction errors and was selected as the final model.

---

## 🖥️ Level 6 — Interactive ML System

The final Machine Learning model was integrated into an interactive **Streamlit web application**.

RailPredict combines:

```text
🤖 ML Prediction
      +
🗺️ Route Exploration
      +
📊 Analytics
      +
💡 Insights
```

into one user-friendly dashboard.

---

# 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| 💻 Programming | Python |
| 🧹 Data Processing | Pandas, NumPy |
| 🤖 Machine Learning | Scikit-learn |
| 📈 Algorithm | Linear Regression |
| 📊 Visualization | Plotly, Matplotlib |
| 🌐 Web Application | Streamlit |
| 📓 Development | Jupyter Notebook, VS Code |
| 🗃️ Version Control | GitHub |

---

# 📁 Project Structure

```text
RailPredict-Train-Journey-Prediction/
│
├── 📂 Dataset/
│   ├── ML Intern Dataset.csv
│   └── ML_Train_Level_Data.csv
│
├── 📂 screenshots/
│   ├── RailPredict_Homepage.png
│   ├── Route_Page.png
│   ├── Train_Analytics.png
│   ├── Train_Insights.png
│   └── Model_Comparision.png
│
├── 📓 Level_1_Data_Understanding.ipynb
├── 📓 Level_2_Data_Cleaning_Feature_Creation.ipynb
├── 📓 Level_3_EDA_Visualization.ipynb
├── 📓 Level_4_Model_Training.ipynb
├── 📓 Level_5_Model_Comparision.ipynb
├── 📓 Level_6_Interactive_System.ipynb
│
├── 🚆 app.py
├── 📋 requirements.txt
├── ⚙️ .gitignore
└── 📝 README.md
```

---

# 🚀 Running RailPredict Locally

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/Rozina-13/RailPredict-Train-Journey-Prediction.git
```

Move into the project:

```bash
cd RailPredict-Train-Journey-Prediction
```

---

## 2️⃣ Create a Virtual Environment

```bash
python -m venv .venv
```

---

## 3️⃣ Activate the Environment

### macOS / Linux

```bash
source .venv/bin/activate
```

### Windows

```bash
.venv\Scripts\activate
```

---

## 4️⃣ Install Requirements

```bash
pip install -r requirements.txt
```

---

## 5️⃣ Run RailPredict 🚆

```bash
streamlit run app.py
```

The RailPredict application will open in your browser.

---

# ⚠️ Project Scope & Limitations

RailPredict predicts the duration of a **complete train journey** using:

```text
Total Distance + Number of Stops
```

The Route Explorer separately provides station-to-station route information.

Therefore, Route Explorer results should **not** be interpreted as separate station-to-station Machine Learning journey-duration predictions.

Prediction performance is also dependent on the patterns, coverage, and quality of the available training data.

---

# 🔮 Future Enhancements

RailPredict could be extended with:

- 🌦️ Weather information
- ⏳ Historical delay information
- 🚦 Operational railway conditions
- 📍 Additional route-related features
- 🤖 Advanced regression algorithms
- 🔍 Model explainability
- ☁️ Cloud deployment
- 🔄 Real-time railway information
- 📈 Additional predictive features

---

# 🎓 Internship Project

<div align="center">

### Machine Learning Internship

## **Sysslan IT Solutions**

This project provided hands-on experience across the complete Machine Learning lifecycle:

**Data Understanding → Data Cleaning → Feature Engineering → EDA → Model Training → Evaluation → Model Comparison → Interactive Application**

</div>

---

# 👩‍💻 Developed By

<div align="center">

## **Rozina Sheereen**

🎓 Final-Year **B.Sc. Artificial Intelligence & Machine Learning** Student

💡 Aspiring **AI / Generative AI Engineer**

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rozina13)

[![GitHub](https://img.shields.io/badge/GitHub-Rozina--13-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Rozina-13)

</div>

---

<div align="center">

## 🚆 RailPredict

### **Turning Railway Data into Intelligent Journey-Time Predictions**

⭐ **Built with Python • Machine Learning • Streamlit**

</div>
