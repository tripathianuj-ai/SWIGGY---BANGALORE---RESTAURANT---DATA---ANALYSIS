# SWIGGY---BANGALORE---RESTAURANT---DATA---ANALYSIS
End-to-end Exploratory Data Analysis of Swiggy restaurant outlets in Bangalore using Python, Pandas, NumPy, Matplotlib, Seaborn and Plotly to uncover insights on ratings, cuisines, locations and cost for two.

🍽️ Swiggy Bangalore Restaurant Data Analysis

End-to-End Exploratory Data Analysis using 

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python) ![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas) ![NumPy](https://img.shields.io/badge/NumPy-Data%20Processing-013243?logo=numpy) ![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange) ![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0) ![Plotly](https://img.shields.io/badge/Plotly-Interactive%20Charts-3F4F75?logo=plotly) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

«An end-to-end Data Analytics project analyzing Swiggy restaurant outlets in Bangalore to uncover actionable insights from restaurant ratings, pricing, cuisines, and locations.»

---

📌 Project Overview

The food delivery industry generates large volumes of restaurant and customer-related data. For businesses, the ability to convert this raw data into meaningful insights is essential for understanding market trends, customer preferences, pricing patterns, and competitive positioning.

This project performs Exploratory Data Analysis (EDA) on Swiggy restaurant outlet data from Bangalore.

The analysis focuses on:

- Restaurant ratings
- Restaurant pricing
- Cuisine categories
- Location-wise restaurant distribution
- Highly-rated restaurants
- Affordable restaurants
- Value-for-money opportunities
- Rating vs. pricing relationships

The project follows a complete real-world Data Analytics workflow:

Raw Data → Data Validation → Data Cleaning → Exploratory Analysis → Visualization → Business Insights

---

🎯 Business Objective

The objective of this analysis is to understand the Bangalore restaurant market and answer key business questions such as:

- How many restaurant records are present in the dataset?
- Is the dataset affected by duplicate records?
- Are there missing values?
- What is the distribution of restaurant ratings?
- What is the distribution of restaurant pricing?
- Which restaurants are highly rated?
- Which restaurants are relatively affordable?
- Which restaurants potentially offer better value for money?
- How are restaurants distributed across Bangalore locations?
- What cuisines are represented in the dataset?
- Is there any visible relationship between restaurant ratings and cost?

---

📊 Dataset

The dataset contains restaurant-level information for Bangalore.

Dataset Features

Column| Description
"Shop_Name"| Name of the restaurant/outlet
"Cuisine"| Cuisine offered by the restaurant
"Location"| Restaurant location
"Rating"| Customer rating
"Cost_for_Two"| Approximate cost for two people

Dataset Size

- 118 restaurant records
- 5 analytical attributes

«The analysis and findings in this repository are based specifically on the dataset used in this project.»

---

🛠️ Tech Stack

Programming

- Python 3.x

Data Analysis

- Pandas
- NumPy

Data Visualization

- Matplotlib
- Seaborn
- Plotly

Environment

- Jupyter Notebook

---

🔄 Analytics Workflow

                 RAW DATA
                    │
                    ▼
            DATA UNDERSTANDING
                    │
                    ▼
          DATA QUALITY CHECKS
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
     Missing Values       Duplicates
          │                   │
          └─────────┬─────────┘
                    ▼
             DATA CLEANING
                    │
                    ▼
          EXPLORATORY ANALYSIS
                    │
          ┌─────────┼─────────┐
          ▼         ▼         ▼
       Ratings    Pricing   Locations
          │         │         │
          └─────────┼─────────┘
                    ▼
            DATA VISUALIZATION
                    │
                    ▼
             BUSINESS INSIGHTS

---

🧹 Data Cleaning & Validation

Data quality checks were performed before beginning the analysis to ensure reliable results.

Dataset Structure

swiggy_data.shape

Used to understand the number of records and attributes.

Dataset Information

swiggy_data.info()

Used to inspect:

- Column names
- Data types
- Non-null values
- Overall dataset structure

Statistical Summary

swiggy_data.describe()

Used to understand the numerical characteristics of the dataset.

Duplicate Check

swiggy_data.duplicated().sum()

Duplicate records were checked to reduce the risk of repeated observations affecting analytical results.

Missing Value Check

swiggy_data.isnull().sum()

Missing values were examined across all important fields.

---

🔎 Exploratory Data Analysis

⭐ 1. Restaurant Rating Analysis

Restaurant ratings were analyzed to understand the overall customer satisfaction pattern within the dataset.

The analysis identifies:

- Rating distribution
- Highly-rated restaurants
- Rating concentration
- Restaurants with strong customer ratings

---

💰 2. Cost Analysis

The "Cost_for_Two" variable was analyzed to understand restaurant pricing patterns.

This helps identify:

- Affordable restaurants
- Higher-priced restaurants
- Common pricing ranges
- Potential value-for-money restaurants

---

📍 3. Location Analysis

Location-wise analysis was performed to understand restaurant distribution across Bangalore.

A focused analysis was also performed for BTM, allowing restaurant ratings and pricing to be studied at a locality level.

Example:

swiggy_data_BTM = swiggy_data[
    swiggy_data["Location"] == "BTM"
]

This demonstrates how the same dataset can be analyzed at both overall-market and locality-specific levels.

---

🍛 4. Cuisine Analysis

Cuisine data was explored to understand the variety of food options represented in the dataset.

Cuisine analysis can support:

- Market segmentation
- Customer preference analysis
- Competitive analysis
- Restaurant positioning

---

⭐ Highly Rated Restaurant Analysis

The analysis identifies highly-rated restaurants based on the "Rating" column.

One of the observations from the dataset was:

🏆 Calicut Cafe Restaurant

Rating: 4.8

This analysis demonstrates how rating-based filtering can be used to identify top-performing restaurants within a dataset.

«Important: These findings represent the project dataset and should not be interpreted as current Swiggy rankings.»

---

💎 Value-for-Money Analysis

A practical business analysis was performed by combining restaurant rating and cost.

For example, restaurants can be segmented using conditions such as:

Rating >= 4.0

and

Cost_for_Two < 500

This helps identify restaurants that combine:

Good Customer Rating + Reasonable Cost

From a business perspective, this approach can support customer recommendations and competitive benchmarking.

---

📈 Visualization & Storytelling

Data visualization was used to convert analytical results into easy-to-understand insights.

Visualizations include:

- ⭐ Rating Distribution
- 💰 Cost Distribution
- 📍 BTM Location Analysis
- 🍛 Cuisine Analysis
- 🏆 Highly-Rated Restaurants
- 💎 Value-for-Money Restaurants
- 📊 Rating vs. Cost Analysis

Visualization Libraries

Matplotlib
Used for foundational analytical charts.

Seaborn
Used for statistical visualization and distribution analysis.

Plotly
Used for interactive visual exploration.

---

📊 Rating vs Cost Analysis

An interactive Plotly scatter plot was created to explore the relationship between restaurant ratings and cost for two people.

Example:

fig = px.scatter(
    high_rated_restaurant,
    x="Rating",
    y="Cost_for_Two",
    color="Rating",
    size="Cost_for_Two"
)

This analysis helps investigate an important business question:

«Do highly-rated restaurants necessarily have higher prices?»

The visualization provides a quick way to compare restaurant quality indicators with pricing.

---

💡 Business Insights

The analysis provides several practical business perspectives.

⭐ Customer Satisfaction

Ratings can be used as an indicator of customer satisfaction and help identify restaurants with strong customer feedback.

💰 Pricing Strategy

Cost analysis can help businesses benchmark restaurant pricing and identify different pricing segments.

💎 Value for Money

Combining ratings with pricing provides a more meaningful customer perspective than looking at either metric independently.

📍 Location Intelligence

Location analysis can help identify restaurant concentration across Bangalore localities and support potential expansion decisions.

🍛 Cuisine Opportunities

Cuisine-level analysis can provide an overview of market diversity and help identify potential opportunities for restaurant positioning.

📊 Competitive Benchmarking

Combining rating, pricing, cuisine and location creates a framework for comparing restaurants within the same market.

---

📌 Key Analytical Questions

Business Question| Analytical Approach
How large is the dataset?| Dataset exploration
Are duplicate records present?| Duplicate analysis
Are there missing values?| Null-value analysis
What is the rating pattern?| Rating distribution
What is the pricing pattern?| Cost distribution
Which restaurants are highly rated?| Rating-based filtering
Which restaurants are affordable?| Cost-based filtering
Which restaurants offer potential value?| Rating + Cost segmentation
How are restaurants distributed by location?| Location analysis
What cuisines are available?| Cuisine analysis
How are rating and cost related?| Interactive scatter plot

---

📂 Project Structure

swiggy-bangalore-restaurant-data-analysis/
│
├── data/
│   └── swiggy_bangalore.csv
│
├── screenshots/
│   ├── rating_distribution.png
│   ├── cost_distribution.png
│   ├── btm_analysis.png
│   └── rating_vs_cost.png
│
├── swiggydataanalysis.ipynb
├── requirements.txt
└── README.md

---

🚀 How to Run

1. Clone the repository

git clone https://github.com/yourusername/swiggy-bangalore-restaurant-data-analysis.git

2. Navigate to the project

cd swiggy-bangalore-restaurant-data-analysis

3. Install dependencies

pip install -r requirements.txt

4. Launch Jupyter Notebook

jupyter notebook

5. Open the notebook

swiggydataanalysis.ipynb

Run the notebook cells sequentially to reproduce the analysis.

---

📦 Requirements

pandas
numpy
matplotlib
seaborn
plotly
jupyter

---

🧠 Data Analyst Skills Demonstrated

🐍 Python

- Python programming
- Pandas
- NumPy
- DataFrame operations
- Conditional filtering

🧹 Data Cleaning

- Data validation
- Missing-value analysis
- Duplicate detection
- Data type inspection

📊 Data Analysis

- Exploratory Data Analysis
- Descriptive statistics
- Data filtering
- Comparative analysis
- Segmentation

📈 Data Visualization

- Matplotlib
- Seaborn
- Plotly
- Histograms
- Scatter plots
- Distribution analysis
- Interactive visualization

💼 Business Analytics

- Pricing analysis
- Customer-oriented analysis
- Location intelligence
- Competitive benchmarking
- Value-for-money analysis
- Business insight generation

---

🚀 Future Enhancements

This project can be further developed into a complete Business Intelligence solution by adding:

- 📊 Power BI dashboard
- 🗃️ SQL-based analysis
- 📍 Location-wise performance dashboard
- 🍛 Cuisine-wise segmentation
- 💰 Advanced pricing analysis
- ⭐ Rating prediction
- 🤖 Restaurant recommendation system
- 🔍 Outlier detection
- 📈 Advanced statistical analysis
- ⚡ Automated data pipeline

---

🎯 Project Impact

This project demonstrates that Data Analytics is not only about writing Python code or creating charts.

The core objective is to transform data into business value:

«Understand the Problem → Validate the Data → Analyze Patterns → Visualize Findings → Generate Business Insights»

The same analytical approach can be applied to industries such as:

- Food Delivery
- E-commerce
- Retail
- Hospitality
- Market Research
- Business Intelligence

---

👨‍💻 About

This project is part of my Data Analytics portfolio, demonstrating practical experience in transforming structured data into meaningful insights using Python.

The project showcases an end-to-end analytical workflow — from data inspection and validation to exploratory analysis, visualization and business interpretation.

Areas of Interest

Data Analytics | Business Intelligence | Python | SQL | Power BI | Excel | Data Visualization

---

⭐ Conclusion

This project demonstrates how restaurant-level data can be transformed into actionable insights around:

Ratings • Pricing • Locations • Cuisines • Customer Value • Competitive Positioning

The project combines technical data-analysis skills with a business-focused approach to problem solving.

---

⭐ If you find this project useful

Feel free to explore the complete notebook and give the repository a ⭐.

Built with Python, curiosity, and a data-driven mindset.
