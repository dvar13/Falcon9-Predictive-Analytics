
# Falcon 9 Landing Prediction Project

This project aims to **predict whether the first stage of the SpaceX Falcon 9 rocket will successfully land** after launch. Predicting landing success helps estimate the **economic viability of launches**, since SpaceX significantly reduces launch costs through **rocket reusability**.

While traditional launch providers charge **over $165M USD per launch**, SpaceX offers Falcon 9 launches for approximately **$62M USD**, largely due to the ability to **recover and reuse the first stage**.

---

#  Project Structure

The workflow is divided into **five main stages**, each documented in its corresponding notebook.

### 1️ Data Collection (API & Web Scraping)

* Extracted technical launch data using the **SpaceX API**
* Performed **web scraping from Wikipedia** to gather additional mission details
* Combined datasets into a unified analysis dataset

---

### 2️ Data Wrangling

* Handled missing values
* **PayloadMass null values** were imputed using the **mean**
* Created the **target variable `Class`**

  * `1` → Successful landing
  * `0` → Failed landing

---

### 3️ Exploratory Data Analysis with SQL

SQL queries were used to explore patterns such as:

* Unique launch sites
* Missions with successful landings
* Payload and orbit relationships
* Launch site distribution

---

### 4️ Data Visualization (EDA)

Visualization tools were used to identify trends and correlations.

Key libraries:

* **Pandas**
* **Matplotlib**
* **Seaborn**

Examples of analysis:

* Flight number vs landing success
* Payload mass vs landing outcome
* Orbit type vs success rate

---

### 5️ Predictive Analysis (Machine Learning)

Machine learning models were trained to **predict landing success**.

Pipeline components included:

* **StandardScaler** for feature scaling
* **GridSearchCV** for hyperparameter tuning
* Model evaluation and comparison

---

# Key Findings

### Increasing Success Rate

The **landing success rate improved significantly between 2013 and 2020**, largely due to SpaceX gaining more experience and increasing the number of launches.

### Optimal Orbits

The following orbits achieved **100% success rate in the analyzed dataset**:

* ES-L1
* GEO
* HEO
* SSO

### Launch Site Influence

Launch sites such as **KSC LC-39A** show higher success rates and are **strategically located near the coast**, facilitating rocket recovery operations.

---

# Machine Learning Models

Several classification models were evaluated:

| Model                        | Accuracy |
| ---------------------------- | -------- |
| Logistic Regression          | ~83%     |
| Support Vector Machine (SVM) | ~83%     |
| K-Nearest Neighbors (KNN)    | ~83%     |
| Decision Tree                | ~83%     |

**Decision Tree** was selected as the **best model** due to its **consistent performance and interpretability**.

---

# Technologies Used

### Programming Language

* **Python**

### Libraries

* **Pandas**
* **NumPy**
* **Scikit-learn**

### Visualization

* **Matplotlib**
* **Seaborn**
* **Folium** (interactive maps)
* **Plotly Dash** (interactive dashboards)

### Databases

* **SQL**
* **SQLite**

---

 **Potential future improvements**

* Incorporate **more recent launch data**
* Test **ensemble models** (Random Forest, Gradient Boosting)
* Deploy the model as an **interactive web application**

---
