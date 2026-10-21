# 🎮 Game Sense – Esports Performance & Gaming Health Analytics

### 📊 Data Analytics Project | Python | Pandas | NumPy | Power BI

**Game Sense** is a data analytics project that explores the relationship between esports players' gaming performance, health indicators, and lifestyle habits. The project analyzes player-session data to understand how sleep, reaction time, Actions Per Minute (APM), energy drink consumption, heart rate, and other factors relate to match outcomes.

Using **Python, Pandas, NumPy, Matplotlib, Seaborn, and Power BI**, the project transforms raw gaming data into meaningful insights that can help players and coaches better understand performance and recovery patterns.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Problem Statement](#-problem-statement)
- [Project Objectives](#-project-objectives)
- [Dataset Information](#-dataset-information)
- [Tools and Technologies](#-tools-and-technologies)
- [Project Workflow](#-project-workflow)
- [Data Cleaning and Feature Engineering](#-data-cleaning-and-feature-engineering)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Key Insights](#-key-insights)
- [Power BI Dashboard](#-power-bi-dashboard)
- [Project Structure](#-project-structure)
- [How to Run the Project](#-how-to-run-the-project)
- [Limitations](#-limitations)
- [Future Improvements](#-future-improvements)
- [Team Members](#-team-members)
- [Dataset Source](#-dataset-source)

---

## 🔍 Project Overview

Esports performance depends on more than gaming skills alone. Lifestyle habits, recovery, and physiological indicators may also be associated with how players perform during matches.

This project analyzes **250,000 player-session records** to investigate patterns between gaming performance and health-related factors.

The analysis focuses on identifying relationships between:

- Sleep duration and match win rate.
- Reaction time and gaming performance.
- APM and match outcomes.
- Energy drink consumption and heart rate.
- Heart Rate Variability (HRV) and sleep duration.
- Game genres and player performance.
- Blue-light filter usage and gaming habits.

The findings are presented through an interactive Power BI dashboard for easier exploration and comparison.

## ❗ Problem Statement

Esports datasets contain valuable information about player performance, lifestyle habits, and physiological conditions. However, raw data alone does not clearly explain how these factors relate to match outcomes.

This project addresses the following questions:

- How is sleep duration associated with match win rates?
- Does faster reaction time correspond to better match outcomes?
- Does a higher APM always indicate better performance?
- How does energy drink consumption relate to heart rate?
- How do performance patterns differ across game genres?
- How are sleep, HRV, and reaction time related?
- How can data visualization help players and coaches explore these relationships?

## 🎯 Project Objectives

- Clean and validate raw esports gaming data.
- Handle missing values and standardize column names.
- Engineer meaningful categories for sleep, APM, and reaction time.
- Perform exploratory data analysis using Python.
- Identify patterns in player performance, health indicators, and lifestyle habits.
- Compare win rates across different game genres and behavioral groups.
- Develop an interactive Power BI dashboard.
- Present data-driven insights that may support training and recovery decisions.

---

## 📂 Dataset Information

| Attribute | Description |
|---|---|
| Dataset Name | Esports Gaming Biometrics Dataset |
| Source | Kaggle |
| Original Records | 250,000 rows |
| Original Columns | 13 |
| Columns After Feature Engineering | 16 |
| Data Type | Player-session-level records |
| Row Meaning | One player's biometric and performance readings for a single match session |

### Important Dataset Columns

| Column | Description |
|---|---|
| `player_id` | Player identifier |
| `age` | Player age |
| `game_genre` | Genre of the game |
| `playtime_hours` | Gaming duration |
| `sleep_hours` | Duration of sleep |
| `energy_drinks` | Energy drink consumption |
| `screen_brightness` | Screen brightness level |
| `blue_light_filter` | Blue-light filter usage |
| `apm` | Actions Per Minute |
| `heart_rate_bpm` | Heart rate in beats per minute |
| `hrv_score` | Heart Rate Variability score |
| `reaction_time_ms` | Reaction time in milliseconds |
| `match_outcome` | Match result |

The dataset combines gaming performance metrics, lifestyle information, and biometric indicators for exploratory analysis.

---

## 🛠️ Tools and Technologies

| Technology | Purpose |
|---|---|
| Python | Data cleaning, transformation, and analysis |
| Pandas | Data manipulation and preprocessing |
| NumPy | Numerical operations and data handling |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Power BI | Interactive dashboard development |
| Jupyter Notebook | Python analysis workflow |
| Microsoft Excel | Storage and inspection of cleaned data |

---

## 🔄 Project Workflow

The project follows a structured data analytics workflow:

**Raw Dataset → Data Cleaning → Feature Engineering → Exploratory Data Analysis → Insights Generation → Power BI Dashboard**

### 1. Data Collection
Collected the Esports Gaming Biometrics Dataset from Kaggle.

### 2. Data Preprocessing
Inspected the dataset, handled missing values, standardized column names, and validated numerical fields.

### 3. Feature Engineering
Created grouped categories to make performance and lifestyle comparisons easier.

### 4. Exploratory Data Analysis
Analyzed relationships between player health indicators, gaming habits, and match outcomes using Python visualization libraries.

### 5. Insights Generation
Identified trends involving sleep, reaction time, APM, energy drink consumption, and game genres.

### 6. Dashboard Development
Designed an interactive Power BI dashboard to present key metrics, comparisons, and analytical findings.

---

## 🧹 Data Cleaning and Feature Engineering

Data cleaning was performed using Python and Pandas.

### Data Cleaning Activities

- **Missing values:** Filled missing values in `screen_brightness` and `hrv_score` using their respective column medians.
- **Duplicate records:** Checked for exact duplicate rows; none required removal.
- **Column standardization:** Converted column names to lowercase.
- **Data validation:** Checked numerical fields, including APM, heart rate, HRV, reaction time, sleep hours, and playtime hours, for invalid negative or zero values.
- **Outlier analysis:** Applied the Interquartile Range (IQR) method to identify potential outliers.
- **Outlier handling:** Retained flagged values because extreme observations could represent legitimate high-intensity gaming sessions or low-recovery conditions.

### Feature Engineering

Created three additional categorical features:

- `sleep_groups` – Groups players according to sleep duration.
- `apm_groups` – Categorizes players by Actions Per Minute.
- `reaction_time_group` – Groups players by reaction time.

These features make it easier to compare win rates and performance indicators across different categories.

---

## 📈 Exploratory Data Analysis

The analysis explored several dimensions of esports performance.

### 1. Performance Analysis

Examined win rates across APM groups and reaction-time categories to understand how these indicators relate to match outcomes.

### 2. Health and Behavioral Analysis

Investigated relationships between:

- Sleep duration and win rate.
- Sleep duration and reaction time.
- Sleep duration and HRV score.
- Energy drink consumption and heart rate.
- Blue-light filter usage and gaming habits.

### 3. Game Genre Analysis

Compared win rates and average HRV scores across:

- Fighting
- MOBA
- FPS
- Battle Royale

### 4. Visualization

Used Matplotlib and Seaborn to explore distributions, trends, and relationships before presenting the findings through Power BI.

---

## 💡 Key Insights

The following findings are based on the project's exploratory analysis.

### 😴 1. Sleep Duration and Win Rate

| Sleep Group | Win Rate |
|---|---:|
| Less than 5 hours | 47.95% |
| 5–7 hours | 50.71% |
| 7–9 hours | 51.61% |
| 9+ hours | 52.12% |

**Insight:** Players in the 9+ hour sleep group had the highest observed win rate, at 52.12%. Longer sleep duration was also associated with lower reaction times and higher HRV scores.

### ⚡ 2. Reaction Time and Performance

| Reaction Time | Win Rate |
|---|---:|
| Less than 220 ms | 50.19% |
| 220–250 ms | 54.20% |
| 250–280 ms | 50.36% |
| 280–310 ms | 46.93% |
| 310+ ms | 44.89% |

**Insight:** The 220–250 ms reaction-time group had the highest observed win rate, at 54.20%. Win rates were lower among groups with reaction times above 280 ms.

### 🎯 3. APM Does Not Guarantee Winning

| APM Group | Win Rate |
|---|---:|
| Less than 100 | 63.64% |
| 100–200 | 44.91% |
| 200–300 | 49.88% |
| 300–400 | 51.71% |
| 400+ | 55.34% |

**Insight:** The lowest APM group had the highest observed win rate. This suggests that a higher action rate alone does not necessarily correspond to better match outcomes.

### ❤️ 4. Energy Drinks and Heart Rate

- Average heart rate increased from approximately 80 BPM among players consuming no energy drinks to approximately 97 BPM among those consuming four.
- The analysis did not identify a clear corresponding improvement in win rate.

**Insight:** Energy drink consumption was associated with higher average heart rates, but the analysis did not establish a direct performance benefit.

### 🎮 5. Performance Across Game Genres

| Game Genre | Win Rate | Average HRV Score |
|---|---:|---:|
| Fighting | 50.63% | 87 |
| MOBA | 49.74% | 87 |
| FPS | 46.46% | 88 |
| Battle Royale | 45.61% | 88 |

**Insight:** Fighting games had the highest observed win rate among the analyzed genres, while Battle Royale had the lowest. Average HRV scores remained relatively similar across genres.

### 💻 6. Blue-Light Filter Usage

Approximately **65% of players** used a blue-light filter.

**Insight:** Blue-light filter usage was common among players in the analyzed dataset.

### 📌 Overall Findings

The analysis highlights relationships between sleep duration, reaction time, energy drink consumption, and esports performance. These patterns may help guide further investigation into gaming habits and recovery.

*Note: These results describe observed associations in the dataset. They do not establish that any single lifestyle factor directly causes a change in match performance.*

---

## 📊 Power BI Dashboard

The Power BI dashboard, titled **Game Sense – Performance & Health Analytics**, brings the project's findings together in an interactive visual interface.

### Dashboard Features

- **KPI Cards:** Total players, win rate, and loss rate.
- **Performance Metrics:** Average APM, reaction time, and sleep duration.
- **Genre Analysis:** Win rates across game genres.
- **Sleep Analysis:** Win rates and performance metrics by sleep group.
- **APM Analysis:** Win rates across APM categories.
- **Reaction-Time Analysis:** Performance comparisons across reaction-time groups.
- **Scatter Plot:** APM versus reaction time, segmented by match outcome.
- **Energy Drink Analysis:** Trends involving energy drink consumption and win rate.
- **Health Metrics:** Average HRV score and heart rate across relevant groups.
- **Blue-Light Filter Analysis:** Usage-share donut chart.
- **Age Analysis:** Player distribution by age group.
- **Interactive Filters:** Game genre, blue-light filter, match outcome, and sleep group.

The dashboard allows users to explore performance patterns, compare player groups, and examine relationships between health indicators and gaming outcomes.

> **Dashboard Preview:** Add your Power BI dashboard screenshots to the repository and embed them here.

Example:

```markdown
![Game Sense Dashboard](images/dashboard-overview.png)
```

---

## 📁 Project Structure

Organize the repository as follows, adjusting the filenames to match your actual uploaded files.

```text
Game-Sense-Esports-Analytics/
│
├── data/
│   ├── game_sense_raw.csv
│   └── gameSense_cleaned.xlsx
│
├── notebooks/
│   └── GameSense.ipynb
│
├── dashboard/
│   └── GameSense.pbix
│
├── images/
│   ├── dashboard-overview.png
│   ├── performance-analysis.png
│   └── health-behavior-analysis.png
│
├── documentation/
│   └── E-Sports Game Sense Documentation.pdf
│
└── README.md
```

*The notebook, Power BI report, and screenshots should be included only if you have those files available. The structure above is a suggested repository layout.*

---

## 🚀 How to Run the Project

### Prerequisites

Install Python and the required libraries.

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Game-Sense-Esports-Analytics.git
```

Replace `YOUR-USERNAME` with your GitHub username.

### Step 2: Navigate to the Project Directory

```bash
cd Game-Sense-Esports-Analytics
```

### Step 3: Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `GameSense.ipynb` and run the cells to reproduce the data cleaning and exploratory analysis, provided the notebook and required dataset are included.

### Step 5: Explore the Power BI Dashboard

Open the `.pbix` report in Microsoft Power BI Desktop to explore the dashboard interactively, provided the report file is included.

---

## ⚠️ Limitations

- The project focuses on descriptive analytics and exploratory data analysis rather than predictive modeling.
- The observed relationships are correlational and do not establish causation.
- The dataset contains individual session records rather than longitudinal tracking of the same players.
- The analysis covers a fixed set of game genres.
- Other factors that influence match outcomes may not be captured in the available dataset.

---

## 🔮 Future Improvements

Potential extensions include:

- Building machine learning models to estimate match win probability.
- Tracking individual players over time to analyze changes in habits and performance.
- Incorporating team, tournament, and coaching data.
- Integrating real-time biometric information during matches.
- Automating dataset refreshes and dashboard updates.
- Adding more detailed dashboard filters and coach-focused views.
- Evaluating model performance if predictive analytics is introduced.

---

## 👥 Team Members

**Team Name:** Data Dynamos

**Institution:** TEKS Academy

**Team Members:**
- Teja Sri
- Ajay Kumar
- Lahari

**Project Type:** Data Analytics Project
## 📚 Dataset Source

The project uses the **Esports Gaming Biometrics Dataset** sourced from Kaggle.

- **Dataset Platform:** Kaggle
- **Dataset:** Esports Gaming Biometrics Dataset

Add the original Kaggle dataset URL here before publishing the repository.

---

## ⭐ Conclusion

Game Sense demonstrates how data analytics can be used to investigate esports performance and gaming health patterns.

By combining Python-based data cleaning, exploratory analysis, and Power BI visualization, the project transforms 250,000 player-session records into interpretable findings about sleep, reaction time, APM, energy drink consumption, and game genres.

The project provides a foundation for further research into player performance, recovery habits, and data-driven esports coaching.
