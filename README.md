# 🏙️ Airbnb Market Dynamics: Chicago vs. New Orleans

## Project Overview
This project is a data analysis of short-term rental markets comparing two major tourist destinations: Chicago and New Orleans. I built this project to help real estate investors and property managers quickly understand the differences between these two markets. By cleaning raw data and creating an interactive dashboard, I uncovered clear patterns about what types of properties perform best and how hosts should price their rentals. 

## Project link
* **Google Colab Notebook:** [Open Data Preprocessing & Analysis Notebook](https://colab.research.google.com/drive/12hpcBdnO7HoZ9bU2eN5d4r1krgAFAlIb?usp=sharing)
* **Power BI Dashboard (.pbix):** [View / Download Power BI Dashboard](https://drive.google.com/file/d/11mqyPkJLFzu0QMJKtQubJeuCQnAloEMR/view?usp=sharing)
## Problem Statement
When investors want to buy short-term rental properties in a new city, they face a lot of uncertainty. High-level national statistics are not helpful because every city has different tourism seasons, pricing limits, and local rules[cite: 10]. This project solves that problem by providing a direct, data-driven comparison of Chicago and New Orleans, helping investors confidently decide where to spend their money and what type of property to buy.

## Project Objectives
*   Merge and clean messy, real-world data from two different cities into a single, usable format.
*   Group complex numbers (like prices and reviews) into simple, easy-to-understand business categories.
*   Compare the true market size, average nightly rates, and most popular property types between the two cities.
*   Build an interactive dashboard that allows stakeholders to easily explore the data without needing to write code.
*   Provide actionable, evidence-based recommendations for property pricing and scaling.

## Dataset Description
The analysis uses two raw datasets: `Chicago_listings (1).csv` and `New Orleans_listings.csv`. 
Combined, the data contains **14,021 active listings** (7,601 in Chicago and 6,420 in New Orleans). 
Important columns include:
*   **Location:** City, neighborhood, latitude, and longitude.
*   **Property Details:** Room type (e.g., entire home vs. private room).
*   **Financials & Activity:** Nightly price, minimum stay requirements, availability, and guest review counts.
*   **Host Information:** Host ID and the number of properties they manage.

## Tools and Technologies
*   **Python (Pandas, NumPy):** Used for loading, combining, cleaning, and transforming the data.
*   **Power BI:** Used to build the final interactive dashboard and charts.
*   **DAX (Data Analysis Expressions):** Used inside Power BI to calculate custom business metrics.

## Project Workflow
1.  **Data Loading & Cleaning:** I combined both datasets and removed rows that were missing critical information, like price or location. I also filled in missing review numbers with zeros.
2.  **Feature Engineering:** I created new categories to make the data easier to analyze. For example, I grouped prices into "Budget" or "Luxury," and categorized hosts as "Casual" (1-2 listings) or "Commercial" (3+ listings).
3.  **Visualization:** I imported the cleaned data into Power BI and designed a four-page interactive report (Overview, Property, Pricing, Host).
4.  **Interpretation:** I analyzed the visual trends to write business recommendations based purely on what the data showed.

## Key Analysis and Findings
*   **Market Size & Price:** Chicago is the larger market (54.21% of listings) and is more expensive, with an average nightly rate of $310 compared to New Orleans' $275.
*   **Property Preferences:** Guests overwhelmingly prefer private spaces. "Entire Home/Apt" listings make up a massive 77.9% of the market (10,926 units), while shared rooms are almost non-existent.
*   **Host Dominance:** The market is run by professionals, not casual homeowners. "Commercial" hosts (managing 3 or more properties) control the majority of listings in both cities. The top host manages 173 properties.
*   **Price Elasticity:** Listings priced between $100 and $200 get the most guest reviews (a sign of high bookings). Demand drops sharply for properties priced over $500.

## Visualizations
The Power BI dashboard contains four main sections:
*   **Overview:** High-level metrics showing total listings, market share donuts, and top neighborhoods.
*   **Property Analysis:** Bar charts showing that "Entire Homes" dominate the market and are mostly available year-round.
*   **Pricing Analysis:** A scatter plot that clearly shows how guest demand drops as prices increase, helping identify the perfect "sweet spot" for pricing.
*   **Host Analysis:** Tables and charts revealing how heavily commercial operators dominate the market compared to everyday people renting out their spare rooms.

## Business Insights and Recommendations
*   **Recommendation 1 (Property Type):** Investors should only buy multi-bedroom "Entire Home" properties. Do not invest in properties meant for shared or private room rentals, as they represent a tiny fraction of market demand.
*   **Recommendation 2 (Pricing Strategy):** To get the most bookings, operators should price their entire-home units between $150 and $225 during normal seasons. Pricing too high will significantly hurt occupancy.
*   **Recommendation 3 (Competitive Strategy):** Independent hosts cannot compete with large commercial operators on volume. They should focus on offering unique, hyper-local guest experiences to win good reviews. 
*   **Recommendation 4 (Regulations):** Hosts should consider setting 3-to-5-night minimum stays during busy weekends to stay compliant with local zoning laws.

## Conclusion
This project successfully transformed raw, messy data from two different cities into a clean, interactive business intelligence tool. I learned how to use Python for complex data preparation and feature engineering, and I improved my ability to use Power BI to tell a clear, actionable data story.

## How to Run the Project
1. Clone this repository to your local machine.
2. Ensure you have Python installed, along with the `pandas` and `numpy` libraries.
3. Run the `data_preprocessing.py` script to see how the raw data is cleaned and transformed.
4. To view the dashboard, download the free version of Power BI Desktop and open the `Airbnb_Market_Dynamics.pbix` file.

## Project Structure
```text
├── data_preprocessing.py                    
├── Chicago_listings (1).csv                 
├── New Orleans_listings.csv                 
├── Cleaned_Airbnb_Chicago_NewOrleans.csv    
├── Airbnb_Market_Dynamics.pbix              
├── Project Report.pdf                       
└── README.md
