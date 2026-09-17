# 🚆 RailPredict — Train Journey Time Prediction System

RailPredict is an end-to-end Machine Learning project developed as part of my Machine Learning Internship at Sysslan IT Solutions.

The system analyzes Indian train schedule and route data and predicts the total journey duration of a train using Machine Learning. The project covers the complete ML workflow — from data understanding and preprocessing to exploratory data analysis, model training, comparison, evaluation, and deployment through an interactive Streamlit dashboard.

---

## 🎯 Project Objective

The main objective of RailPredict is to build a Machine Learning system capable of predicting train journey duration using important journey characteristics.

The project focuses on:

- Understanding and inspecting train journey data
- Cleaning and preprocessing raw schedule data
- Engineering useful Machine Learning features
- Analyzing relationships between journey characteristics
- Training and evaluating prediction models
- Comparing different feature configurations
- Building an interactive prediction system

---

## 📊 Dataset

The project uses train schedule and route information containing details such as:

- Train number
- Station name
- Arrival time
- Departure time
- Distance
- Stop sequence

The raw station-level dataset is processed and transformed into a train-level Machine Learning dataset.

### Machine Learning Features

**Input Features (X):**

- `Total_Distance`
- `Number_of_Stops`

**Target Variable (y):**

- `Journey_Duration_Minutes`

---

## 🧠 Machine Learning Workflow

The internship project was completed through six levels.

### Level 1 — Understanding the Data

- Inspected dataset size and structure
- Examined columns and data types
- Identified train-wise starting and ending stations
- Calculated descriptive statistics
- Checked missing values
- Checked duplicate records
- Identified incorrect or inconsistent values

### Level 2 — Data Cleaning & Feature Creation

- Cleaned the train schedule dataset
- Handled missing and duplicate data
- Converted arrival and departure times into a usable format
- Calculated complete journey duration for each train
- Created total distance as a feature
- Created number of stops as a feature
- Generated the train-level Machine Learning dataset

### Level 3 — Exploratory Data Analysis

Exploratory Data Analysis was performed to understand relationships within the data.

Visualizations include:

- Distance vs Journey Duration
- Number of Stops vs Journey Duration
- Correlation analysis
- Train-wise stop analysis
- Pivot-table based exploration

### Level 4 — Model Training & Evaluation

The dataset was divided into training and testing sets using an 80/20 split.

A **Linear Regression** model was trained using:

- Total Distance
- Number of Stops

The model was evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score
- Actual vs Predicted visualization

### Model Performance

| Metric | Result |
|---|---:|
| MAE | ~58.73 minutes |
| RMSE | ~157.58 minutes |
| R² Score | ~0.945 |

The R² score indicates that the model explains a large proportion of the variation in journey duration within this dataset.

---

## ⚖️ Level 5 — Model Comparison

Two Linear Regression configurations were compared.

### Model 1 — Distance Only

Uses:

`Total_Distance`

Performance:

- MAE: ~67.51 minutes
- RMSE: ~167.48 minutes

### Model 2 — Distance + Stops

Uses:

`Total_Distance`
`Number_of_Stops`

Performance:

- MAE: ~58.73 minutes
- RMSE: ~157.58 minutes
- R²: ~0.945

### Final Model Selection

The **Distance + Stops Linear Regression model** achieved lower MAE and RMSE compared with the Distance Only model.

Therefore, the **Distance + Stops model was selected as the final model** for train journey duration prediction.

---

## 🖥️ Level 6 — Interactive ML System

The final Machine Learning system was developed as an interactive **Streamlit web application** called **RailPredict**.

The application provides a user-friendly interface for interacting with the trained model and exploring train routes.

### RailPredict Features

#### 🚆 Journey Prediction

Users can enter:

- Total journey distance
- Number of stops

The Machine Learning model predicts the estimated duration of the complete train journey.

#### 🗺️ Route Explorer

Users can:

- Select a starting station
- Select a valid destination station
- View trains operating between the selected stations
- Explore station sequences
- View arrival and departure information
- Calculate route distance
- View the number of stops

#### 📊 Analytics

Interactive visualizations help explore:

- Journey distance
- Journey duration
- Number of stops
- Model behavior
- Dataset patterns

#### 💡 Insights

The dashboard presents important observations derived from the processed train journey dataset and Machine Learning analysis.

---

## 🛠️ Technologies Used

### Programming
- Python

### Data Processing
- Pandas
- NumPy

### Machine Learning
- Scikit-learn
- Linear Regression
- Train/Test Split
- MAE
- RMSE
- R²

### Data Visualization
- Plotly

### Web Application
- Streamlit

### Development Tools
- Jupyter Notebook
- Visual Studio Code
- Git
- GitHub

---

## 📁 Project Structure

```text
SYSSLAN_INTERNSHIP/
│
├── Dataset/
│   ├── ML Intern Dataset.csv
│   └── ML_Train_Level_Data.csv
│
├── app.py
│
├── Level_1_Data_Understanding.ipynb
├── Level_2_Data_Cleaning_Feature_Creation.ipynb
├── Level_3_EDA_Visualization.ipynb
├── Level_4_Model_Training.ipynb
├── Level_5_Model_Comparision.ipynb
├── Level_6_Interactive_System.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore