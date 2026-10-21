# 📱 Mobile App User Engagement and Subscription Analysis

### Data Analytics Project | Python | Pandas | NumPy | Power BI

## 📌 Project Overview

**Mobile App User Engagement and Subscription Analysis** is a data analytics project that explores user interactions, device usage, application engagement, and subscription patterns.

The project uses Python for data cleaning, preprocessing, and exploratory data analysis (EDA), followed by Power BI for interactive dashboard development.

The goal is to understand how users interact with a mobile application, identify the most frequently used devices and features, compare Android and iOS activity, and discover opportunities to improve engagement and subscription conversion.

📊 **Project Highlights**
- Analyzed 100,000 raw user interaction records.
- Cleaned dataset containing 98,656 records and 21 columns.
- Compared Android and iOS interaction volumes.
- Identified frequently used event types and device models.
- Explored subscription distribution and checkout interactions.
- Developed an interactive Power BI dashboard.

---

## 🎯 Project Objectives

- Clean and prepare the raw mobile app interaction dataset.
- Identify the most frequently used operating systems and mobile devices.
- Analyze user engagement through interaction events and session duration.
- Compare user activity across Android and iOS platforms.
- Examine subscription patterns among users.
- Identify the most frequently interacted-with app features.
- Explore relationships between numerical variables.
- Build an interactive Power BI dashboard to communicate insights.
- Provide data-driven recommendations for engagement and subscription growth.

---

## ❓ Problem Statement

Mobile applications generate large amounts of user interaction data, including device information, user demographics, session activity, event types, battery levels, memory usage, and subscription status.

However, raw data alone does not clearly reveal which devices and platforms generate the most engagement, which application features receive the most interactions, or how subscription status relates to user activity.

Missing and inconsistent values can also make it difficult to analyze the data accurately.

This project addresses these challenges by cleaning and analyzing mobile app interaction data using Python and transforming the findings into an interactive Power BI dashboard.

The analysis aims to help answer important business questions:

- Which operating system generates the most user interactions?
- Which mobile device models are used most frequently?
- What are the most common types of user interactions?
- Which application elements receive the most engagement?
- What proportion of users have active subscriptions?
- How do session duration, memory usage, battery level, and user age relate to one another?
- Where are the opportunities to improve user engagement and subscription conversion?

---

## 📂 Dataset Information

The project uses the Mobile App Interaction Dataset.

| Attribute | Details |
|---|---|
| Dataset Name | Mobile App Interaction Dataset |
| Original Records | 100,000 |
| Original Columns | 21 |
| Cleaned Records | 98,656 |
| Cleaned Columns | 21 |
| Data Type | User session and event interaction data |
| Dataset Source | `mobile_app_user_interactions.csv` |
| Cleaned File | `mobile_app_user_interactions_cleaned.xlsx` |
| Analysis Environment | Google Colab |

Each row represents a single user session or event interaction.

### Important Dataset Columns

| Column | Description |
|---|---|
| `date` | Date and time of the interaction |
| `user_id` | Unique user identifier |
| `session_id` | Unique session identifier |
| `device_os` | Device operating system, such as Android or iOS |
| `device_os_version` | Operating system version |
| `device_model` | Mobile device model |
| `screen_resolution` | Device screen resolution |
| `location_country` | User's country |
| `location_city` | User's city |
| `app_language` | Application language setting |
| `network_type` | Network connection type |
| `battery_level` | Battery level at the time of interaction |
| `memory_usage_mb` | Application memory usage |
| `event_type` | Type of user interaction |
| `event_target` | Application element targeted by the interaction |
| `event_value` | Numeric value associated with the event |
| `session_duration_sec` | Session duration in seconds |
| `is_subscribed` | Whether the user has an active subscription |
| `user_age` | User age |
| `push_enabled` | Whether push notifications are enabled |

---

## 🛠️ Tools and Technologies

| Tool | Purpose |
|---|---|
| Python | Data cleaning, preprocessing, and analysis |
| Pandas | Data manipulation and transformation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Google Colab | Python notebook environment |
| Microsoft Power BI | Interactive dashboard development |
| Microsoft Excel | Storage and inspection of cleaned data |

---

## 🔄 Project Workflow

The project follows a structured data analytics workflow:

**Data Collection → Data Inspection → Data Cleaning → Exploratory Data Analysis → Insight Generation → Power BI Dashboard**

### 1. Data Collection
Loaded the mobile app interaction dataset into Python for analysis.

### 2. Data Inspection
Examined the dataset's shape, column names, data types, summary statistics, missing values, and duplicate records.

### 3. Data Cleaning
Handled missing values, standardized data types, removed records with missing identifiers, and investigated numerical outliers.

### 4. Exploratory Data Analysis
Analyzed operating system usage, subscription distribution, interaction types, device models, event targets, and numerical correlations.

### 5. Insight Generation
Identified patterns that could inform platform prioritization, checkout optimization, and subscription conversion strategies.

### 6. Dashboard Development
Built an interactive Power BI dashboard to present engagement metrics and subscription-related findings.

---

## 🧹 Data Cleaning and Preprocessing

Data cleaning was performed using Python and Pandas.

### Data Cleaning Steps

**1. Initial Inspection**
- Examined dataset dimensions and sample records.
- Reviewed data types and summary statistics.
- Checked for duplicate rows.
- Identified missing values across the 21 columns.

**2. Sparse Column Analysis**
- Evaluated columns using a 50% non-missing-value threshold.
- Retained all 21 columns because none exceeded the specified missing-value threshold.

**3. Data Type Conversion**
- Converted the `date` column into datetime format.
- Reviewed unique values in important categorical columns.
- Standardized numerical column types where required.

**4. Missing Value Handling**
- Removed rows with missing `ip_address`, `session_id`, or `user_id`.
- Filled missing categorical values using the mode.
- Filled missing numerical values using the mean where appropriate.
- Used the median for `device_os_version` because it contained outliers.

**5. Outlier Detection**
- Used boxplots to inspect numerical variables.
- Applied the Interquartile Range (IQR) method to `device_os_version`.
- Retained valid `session_duration_sec` values without IQR filtering because the analysis did not identify outliers in that column.

**6. Export**
- Exported the cleaned dataset to Excel for further analysis and visualization.

### Dataset After Cleaning

| Metric | Value |
|---|---:|
| Original Rows | 100,000 |
| Cleaned Rows | 98,656 |
| Original Columns | 21 |
| Cleaned Columns | 21 |
| Rows Removed | 1,344 |

---

## 📊 Exploratory Data Analysis

Exploratory Data Analysis was performed using Pandas, Matplotlib, and Seaborn.

### Analysis Areas

**1. Operating System Analysis**
- Compared interactions between Android and iOS.
- Identified the dominant platform by interaction volume.

**2. Subscription Analysis**
- Examined the distribution of subscribed and non-subscribed users.
- Identified potential opportunities for subscription conversion.

**3. Event Type Analysis**
- Compared the frequency of different user interaction events.
- Identified the most common interaction types.

**4. Device Model Analysis**
- Ranked mobile device models by interaction count.
- Identified the device model generating the most interactions.

**5. Event Target Analysis**
- Examined interactions with different application interface elements.
- Identified the most frequently engaged event target.

**6. Correlation Analysis**
- Investigated relationships between battery level, memory usage, event value, session duration, and user age.
- Used a heatmap to visualize linear correlations.

---

## 💡 Key Insights and Findings

The following insights are based on the project's analysis and documentation.

### 1. Android Dominates Interaction Volume

Android generated significantly more interactions than iOS.

The Xiaomi Mi 11 was the leading device model by interaction count.

**Business implication:** Prioritize understanding the Android user experience while continuing to monitor performance and engagement across iOS devices.

### 2. Subscription Distribution Is Nearly Evenly Split

The analysis found that slightly more than half of users were subscribed.

The remaining non-subscribed users represent a potential audience for subscription-conversion initiatives.

**Business implication:** Investigate targeted campaigns, onboarding improvements, and subscription messaging to encourage appropriate conversion.

### 3. Clicks Are the Most Common Interaction

Click was the most frequently recorded event type, followed by share and view.

The distribution suggests that users engage with multiple types of application interactions.

**Business implication:** Monitor common interaction paths to understand how users navigate the application and which features receive the most attention.

### 4. Checkout Is a Key Interaction Point

The checkout button was the most frequently engaged event target in the analysis.

This indicates substantial interaction with the application's purchasing or conversion area.

**Business implication:** Examine the checkout experience to identify opportunities to simplify navigation, improve usability, and support successful conversions.

### 5. Numerical Usage Metrics Have Weak Linear Relationships

The correlation analysis found weak linear relationships among battery level, memory usage, event value, session duration, and user age.

**Business implication:** User engagement should not be explained using any single one of these variables in isolation. Additional analysis may be needed to identify more complex relationships.

### Summary of Findings

| Analysis Area | Key Finding | Potential Business Action |
|---|---|---|
| Operating Systems | Android has more interactions than iOS | Investigate Android engagement and usability |
| Device Models | Xiaomi Mi 11 leads in interaction count | Examine high-activity device segments |
| Subscriptions | Slightly more than half of users are subscribed | Explore subscription conversion opportunities |
| Event Types | Click is the most frequent interaction | Analyze common user interaction paths |
| Event Targets | Checkout button receives the most interactions | Review the checkout experience |
| Correlation Analysis | Numerical variables show weak linear relationships | Explore additional explanatory factors |

*These are descriptive findings from the available dataset. They do not establish causation or prove that a particular product change will improve engagement or subscription conversion.*

---

## 📈 Power BI Dashboard

The project includes an interactive dashboard titled:

**Mobile App User Interaction Dashboard**

The dashboard presents engagement metrics, device comparisons, subscription information, and session behavior.

### Dashboard Page 1: Engagement Overview

Key visualizations include:

- Total interactions.
- Average session duration.
- Average memory usage.
- Subscription rate.
- Interactions by event type.
- Subscription rate by country.
- Interaction count by operating system.
- Top mobile device models.
- Subscription distribution by device OS.
- Top countries by mobile user count.

### Dashboard Page 2: Detailed Analysis

Key visualizations include:

- Average session duration by device OS.
- Average event value by event type.
- Memory usage versus session duration by device model.
- Average battery level by network type.
- Interaction counts by event type and event target.
- Top device models by session duration.

### Dashboard Purpose

The dashboard enables users to explore overall engagement, compare operating systems, identify popular devices and application elements, and examine subscription patterns.

### Dashboard Preview

Add screenshots of your Power BI dashboard to your GitHub repository.

For example:

```markdown
![Mobile App Dashboard Overview](images/dashboard-page-1.png)

![Mobile App Detailed Analysis](images/dashboard-page-2.png)
```

The screenshots will appear in the README after you upload the corresponding image files.

---

## 📁 Project Structure

A suggested GitHub repository structure is:

```text
Mobile-App-Engagement-Analytics/
│
├── data/
│   └── mobile_app_user_interactions_cleaned.xlsx
│
├── notebooks/
│   └── mobile_app_user_engagement_analysis.ipynb
│
├── dashboard/
│   └── Mobile_App_User_Interaction_Dashboard.pbix
│
├── images/
│   ├── dashboard-page-1.png
│   └── dashboard-page-2.png
│
├── documentation/
│   └── Mobile_App_User_Engagement_and_Subscription_Analytics_Documentation.docx
│
└── README.md
```

*This is a recommended structure. Include the notebook, Power BI report, screenshots, and documentation only when the corresponding files are available.*

---

## 🚀 How to Run the Project

### Prerequisites

Install Python and the required libraries.

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Mobile-App-Engagement-Analytics.git
```

Replace `YOUR-USERNAME` with your GitHub username.

### Step 2: Navigate to the Project Directory

```bash
cd Mobile-App-Engagement-Analytics
```

### Step 3: Install the Required Libraries

```bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

### Step 4: Open Jupyter Notebook

```bash
jupyter notebook
```

Open the project notebook and execute the cells to reproduce the analysis, provided the notebook and required dataset are included.

Alternatively, upload the notebook and dataset to Google Colab and run the analysis there.

### Step 5: Open the Power BI Dashboard

Open the `.pbix` report in Microsoft Power BI Desktop to explore the dashboard interactively, provided the report file is included.

---

## ⚠️ Limitations

- The project focuses on descriptive and exploratory analytics rather than predictive modeling.
- Correlations do not establish causal relationships.
- Missing-value imputation may reduce some natural variability in the data.
- The dashboard does not yet provide detailed city-level and age-group segmentation.
- Weak linear correlations do not rule out nonlinear relationships.
- The analysis does not establish why particular users subscribe or which factors directly drive conversion.

---

## 🔮 Future Improvements

Potential extensions include:

- Adding time-based engagement and subscription trend analysis.
- Performing cohort analysis to understand how user behavior changes over time.
- Segmenting engagement by country, city, and age group.
- Building machine learning models to predict subscription conversion.
- Exploring nonlinear relationships among user engagement metrics.
- Incorporating marketing campaign and revenue data.
- Improving Power BI dashboard filtering and drill-down capabilities.
- Investigating checkout interactions in greater detail.


## 🏁 Conclusion

The Mobile App User Engagement and Subscription Analysis project demonstrates how Python-based data analytics and Power BI visualization can transform raw mobile application interactions into useful business insights.

The analysis identified Android as the dominant platform by interaction volume, the Xiaomi Mi 11 as the leading device model, click as the most common event type, and the checkout button as the most-engaged event target.

The subscription distribution also indicated opportunities to investigate conversion strategies, while weak linear correlations among numerical variables highlighted the need for further analysis.

These findings can support future investigations into mobile app usability, engagement patterns, and subscription growth.

