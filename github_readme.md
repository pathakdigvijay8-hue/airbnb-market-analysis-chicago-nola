# 🏙️ Airbnb Market Dynamics: Chicago vs. New Orleans

## 📌 Project Overview
This repository contains a comparative data analysis of the short-term rental markets in Chicago and New Orleans. By processing raw Airbnb listing data using **Python (Pandas, NumPy)** and visualizing the results in a 4-page interactive **Power BI** dashboard, this project uncovers critical market dynamics regarding pricing elasticity, property composition, and the professionalization of Airbnb hosts.

**Total Processed Listings:** 14,021 (Chicago: 7,601 | New Orleans: 6,420)
**Combined Average Nightly Rate:** $294.40

## 📂 Repository Structure
```text
├── data/
│   ├── Chicago_listings (1).csv
│   ├── New Orleans_listings.csv
│   └── Cleaned_Airbnb_Chicago_NewOrleans.csv  # Final output from Python
├── scripts/
│   └── data_preprocessing.py                  # Python cleaning and feature engineering script
├── dashboard/
│   └── Airbnb_Market_Dynamics.pbix            # Interactive Power BI file
├── images/
│   └── dashboard_screenshots/                 # Folder containing screenshots of the Power BI report
├── Project_Report.md                          # Comprehensive detailed analysis report
└── README.md                                  # Project overview and instructions
```

## 🛠️ Tech Stack
* **Python (Pandas, NumPy):** Data ingestion, cleaning, text standardization, and feature engineering.
* **Power BI & DAX:** Interactive data visualization, KPI aggregations, and dashboard design.

## 📄 Detailed Report
For a deep dive into the methodology, data cleaning logic, exploratory data analysis, and strategic business recommendations, please read the full **[Project Report](Project_Report.md)** included in this repository.

## 🚀 How to Run
1. Clone this repository to your local machine.
2. Run `data_preprocessing.py` to process the raw CSVs and generate the cleaned combined dataset.
3. Open `Airbnb_Market_Dynamics.pbix` in Power BI Desktop to interact with the visualizations.