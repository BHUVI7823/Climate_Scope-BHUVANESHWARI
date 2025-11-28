🌦️ ClimateScope Weather Dashboard — README
📌 Project Overview

This project analyzes global weather data and builds an interactive Power BI dashboard to study temperature, humidity, wind speed, pressure, and country-wise climate patterns.

I used a dataset named GlobalWeatherRepository_cleaned.csv, which I cleaned myself after performing a complete Exploratory Data Analysis (EDA) in Python.
The final output is an interactive dashboard built using Power BI Desktop.

📁 Project Structure
📦 ClimateScope Dashboard Project
|–– 📄 CLIMATE_SCOPE.ipynb        # Python EDA and data-cleaning notebook
|–– 📄 GlobalWeatherRepository_cleaned.csv   # Final cleaned dataset
|–– 📄 Bhuvana-climatescope dashboard.pbix   # Power BI dashboard file
|–– 📄 README.md                   # Documentation (this file)

🧹 1. Data Cleaning & Preprocessing (Python)

I used Python to clean and prepare the dataset.
The EDA and cleaning steps were done inside CLIMATE_SCOPE.ipynb.

✔️ Steps Performed
1. Imported Required Libraries

pandas

numpy

matplotlib

seaborn

These were used for data loading, inspection, cleaning, and visualization.

2. Loaded the Raw Dataset

I loaded the dataset and checked:

Column names

Number of rows

Shape and datatypes

Missing values

Duplicate rows

3. Identified Important Columns

Using column name patterns, I filtered:

Temperature columns

Humidity columns

Wind-related columns

Pressure columns

This helped me understand the weather metrics properly.

4. Cleaned Temperature Data

Some columns had values in Fahrenheit, so I converted them to Celsius.

Formula used:

(TempF - 32) * 5/9

5. Handled Missing Values

If a column had very few missing values → filled using mean/median.

If a column had too many missing values → removed the column.

Completely empty columns → dropped.

6. Removed Invalid or Extreme Values

Examples:

Temperatures like 500°C

Negative humidity

Impossible wind speeds

Such values were removed to maintain dataset accuracy.

7. Checked for Duplicates

All duplicate rows were dropped.

8. Standardized Time Column

Converted timestamps into a readable format:

Year

Month

Day

Hour

This helped in time-based analysis in Power BI.

9. Final Export

After cleaning, I exported the dataset as:

GlobalWeatherRepository_cleaned.csv


This dataset is the one used to build the dashboard.

📊 2. Exploratory Data Analysis (EDA)

Before cleaning, I performed EDA to understand the dataset better.

✔️ EDA Process Includes:
1. Understanding Data Shape

Number of countries

Number of cities

Time range

2. Summary Statistics

Found mean, max, min, median for:

Temperature

Humidity

Wind speed

Pressure

3. Outlier Detection

Using:

Box plots

Histograms

Value counts

4. Correlation Analysis

Checked relationships between:

Temperature vs humidity

Humidity vs pressure

Wind vs temperature

5. Visualization

Plotted:

Distribution graphs

Heatmaps

Line charts

Bar charts

These insights helped shape the Power BI visuals.

📈 3. Power BI Dashboard

The dashboard file is:

Bhuvana-climatescope dashboard.pbix

✔️ Steps Performed in Power BI
1. Imported Cleaned CSV

Loaded GlobalWeatherRepository_cleaned.csv into Power BI.

2. Performed Transformations (if required)

Changed data types

Renamed columns

Created calculated columns

Created measures

3. Built Visuals

The dashboard contains visuals like:

🌡️ Temperature Analysis

Average temperature per country

Max/Min temperature

Monthly trends

💧 Humidity Analysis

Average humidity

Trend by country

Range distribution

🌬️ Wind & Pressure Analysis

Wind speed variations

Pressure comparison globally

🗺️ Interactive Map

Shows:

Cities

Country-wise weather metrics

📌 KPIs

Highest temperature

Lowest temperature

Average humidity

Average wind speed

🎨 Design Choices

Light background for better readability

Contrast colors for charts

Clear fonts and proper spacing

Tooltips for better user experience

Page -1 Global Climate Overview

<img width="1165" height="657" alt="image" src="https://github.com/user-attachments/assets/ac65a406-ddf5-4eb8-94f4-d4d068bc7263" />


Page -2 Renewable and emissions trends

<img width="1162" height="793" alt="image" src="https://github.com/user-attachments/assets/dcf0f108-d784-4fe8-8dbd-083c660f8795" />


🛠️ Tools & Technologies Used
Tool	Purpose
Python (Colab Notebook)	Data cleaning, EDA
pandas / numpy	Data manipulation
matplotlib / seaborn	Visualizations
Power BI Desktop	Dashboard creation
CSV File	Final cleaned dataset
🚀 How to Use This Project
1. Open the Cleaned Dataset

File: GlobalWeatherRepository_cleaned.csv

2. Run EDA Notebook

File: CLIMATE_SCOPE.ipynb

3. Open the Dashboard

Use Power BI Desktop to open:

Bhuvana-climatescope dashboard.pbix

🧾 Conclusion

This project shows the complete workflow of:

Importing raw weather data

Performing EDA

Cleaning and validating the dataset

Building an interactive dashboard in Power BI

It gives clear insights into global weather patterns and helps understand climate behavior on a country level.
