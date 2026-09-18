#  Football Player Performance Analysis Using Machine Learning

##  Project Overview

Football player performance is influenced by many different statistical indicators. A single statistic cannot fully represent a player's performance, especially because **forwards, midfielders, and defenders have different roles and responsibilities**.

This project uses **Exploratory Data Analysis (EDA)** and **Machine Learning** to analyze football player statistics, classify players into different performance levels, and identify the factors that contribute most to performance classification.

The project compares two ensemble learning algorithms:

 **Random Forest**
*  **XGBoost**

The goal is to combine **performance analysis, machine learning, and feature importance** to provide a more data-driven understanding of football player performance.

---

## Objectives

1. **Understand Player Performance**

   * Analyze statistical indicators used to describe football player performance.
   * Consider the different responsibilities of forwards, midfielders, and defenders.

2. **Classify Performance**

   * Categorize players into:

     * Low
     * Medium
     * High

3. **Compare Machine Learning Models**

   * Compare Random Forest and XGBoost for performance classification.

4. **Identify Important Factors**

   * Determine which football statistics contribute most strongly to the model's predictions.

---

## Dataset

The project uses a football player statistics dataset containing information across multiple seasons.

### Dataset Overview

| Description                        |              Value |
| ---------------------------------- | -----------------: |
| Original Records                   |             92,170 |
| Original Features                  |                120 |
| Seasons Considered                 | 2017–18 to 2024–25 |
| Positions Considered               |         FW, MF, DF |
| Records After Position Filtering   |             24,034 |
| Records After 450-Minute Filter    |             14,812 |
| Duplicate Player-Season Groups     |                223 |
| Final Unique Player-Season Records |             14,589 |

The dataset contains various football performance statistics that are used during analysis and performance scoring.

---

## Exploratory Data Analysis (EDA)

EDA was performed to understand the dataset before applying performance scoring and machine learning.

The analysis includes:

* Dataset size and structure
* Season distribution
* Player position distribution
* League-related information
* Position-wise record distribution
* Records across different seasons
* Performance-level distribution
* Missing-value inspection
* Duplicate player-season identification

### Position Distribution

After filtering for the relevant positions:

* **Defenders (DF):** 9,338
* **Midfielders (MF):** 8,380
* **Forwards (FW):** 6,316

### Performance-Level Distribution

The final dataset contains:

* **Low:** 3,646 players
* **Medium:** 7,303 players
* **High:** 3,640 players

---

## Data Preparation

The project applies several steps before machine learning:

1. Select relevant seasons.
2. Select forwards, midfielders, and defenders.
3. Filter players based on a minimum of **450 minutes played**.
4. Identify duplicate player-season records.
5. Combine duplicate player-season groups.
6. Calculate performance-related statistics.
7. Generate position-specific performance scores.
8. Categorize players into Low, Medium, and High performance levels.

---

## Performance Scoring

Because different positions have different responsibilities, the project uses **position-specific performance scoring**.

Different statistics are given different weights depending on whether the player is:

* ⚽ Forward
* 🎯 Midfielder
* 🛡️ Defender

The resulting performance score is converted to a **0–100 scale** and used to create the performance classes.

---

##  Machine Learning Models

## Random Forest

Random Forest is an ensemble learning algorithm that builds multiple decision trees and combines their predictions.

It was selected because it:

* Handles many features.
* Captures nonlinear relationships.
* Works well with numerical football statistics.
* Provides feature-importance information.
* Provides an interpretable baseline for comparison.

### XGBoost

XGBoost is a gradient-boosting algorithm that builds decision trees sequentially.

It was selected because it:

* Provides strong predictive performance.
* Learns from errors made by previous trees.
* Captures nonlinear relationships.
* Can model interactions between different football statistics.
* Provides feature-importance information.

---

## Model Analysis

The project compares Random Forest and XGBoost based on their classification performance.

Feature-importance analysis is also performed to understand which football statistics have the greatest contribution to the predictions.

The project includes visualizations for:

* Random Forest feature importance
* XGBoost feature importance
* Combined feature importance
* Random Forest vs XGBoost accuracy

---

## Repository Structure

```text
Football-Player-Performance-Analysis/
│
├── 📄 README.md
│
├── 📊 All_Players_1992-2025.csv
│
├── 📓 ML_Project (2) (1).ipynb
│
├── 📓 Football_Player_EDA_Only.ipynb
│
├── 📑 Football_Player_Performance_Analysis_Theoretical_PPT_Final_with_EDA.pptx
│
└── 📄 Abstract
```

> **Note:** The dataset file is relatively large, so depending on the GitHub repository setup, it may be better to use Git LFS or provide the dataset through an external source.

---

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **XGBoost**
* **Matplotlib**
* **Jupyter Notebook**
* **Google Colab / Jupyter**

---

## Project Workflow

```text
Football Player Dataset
          ↓
     Data Loading
          ↓
Exploratory Data Analysis
          ↓
Season & Position Filtering
          ↓
450-Minute Filtering
          ↓
Duplicate Identification
          ↓
Feature Preparation
          ↓
Position-Specific Performance Score
          ↓
Performance Classification
     ↓        ↓
Random     XGBoost
Forest
     ↓        ↓
Feature Importance
          ↓
Model Comparison
          ↓
Performance Analysis
```

---

## Why This Analysis Matters

### Position-Aware Evaluation

A forward, midfielder, and defender contribute to a team in different ways. Therefore, player performance should consider the responsibilities associated with each position.

### Data-Driven Decisions

Statistical analysis can support:

* Player comparison
* Scouting
* Recruitment
* Coaching
* Performance evaluation

### Interpretability

Feature importance helps explain **which statistics are important to the model's predictions**, rather than only producing a performance classification.

---

 Future Scope

The project can be extended by:

* Including more leagues and seasons.
* Adding richer match and tactical information.
* Improving model hyperparameter tuning.
* Exploring additional machine learning algorithms.
* Using advanced explainability techniques such as **SHAP**.
* Incorporating additional player and match context.

---

 Project Focus

This project demonstrates how **Exploratory Data Analysis and Machine Learning** can be combined to study football player performance and identify meaningful statistical factors associated with different performance levels.

---

##  License

This project is created for **academic and educational purposes**.
