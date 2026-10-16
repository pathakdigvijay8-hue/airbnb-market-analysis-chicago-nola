# 🏙️ Airbnb Market Dynamics: Chicago vs. New Orleans

## Project Overview
This project is a data analysis of short-term rental markets comparing two major tourist destinations: Chicago and New Orleans[cite: 10]. I built this project to help real estate investors and property managers quickly understand the differences between these two markets. By cleaning raw data and creating an interactive dashboard, I uncovered clear patterns about what types of properties perform best and how hosts should price their rentals[cite: 16, 17]. 

## Problem Statement
When investors want to buy short-term rental properties in a new city, they face a lot of uncertainty. High-level national statistics are not helpful because every city has different tourism seasons, pricing limits, and local rules[cite: 10]. This project solves that problem by providing a direct, data-driven comparison of Chicago and New Orleans, helping investors confidently decide where to spend their money and what type of property to buy.

## Project Objectives
*   Merge and clean messy, real-world data from two different cities into a single, usable format[cite: 11].
*   Group complex numbers (like prices and reviews) into simple, easy-to-understand business categories[cite: 11].
*   Compare the true market size, average nightly rates, and most popular property types between the two cities[cite: 11].
*   Build an interactive dashboard that allows stakeholders to easily explore the data without needing to write code[cite: 11].
*   Provide actionable, evidence-based recommendations for property pricing and scaling[cite: 11].

## Dataset Description
The analysis uses two raw datasets: `Chicago_listings (1).csv` and `New Orleans_listings.csv`[cite: 10]. 
Combined, the data contains **14,021 active listings** (7,601 in Chicago and 6,420 in New Orleans)[cite: 10]. 
Important columns include:
*   **Location:** City, neighborhood, latitude, and longitude.
*   **Property Details:** Room type (e.g., entire home vs. private room).
*   **Financials & Activity:** Nightly price, minimum stay requirements, availability, and guest review counts.
*   **Host Information:** Host ID and the number of properties they manage.

## Tools and Technologies
*   **Python (Pandas, NumPy):** Used for loading, combining, cleaning, and transforming the data[cite: 10, 11].
*   **Power BI:** Used to build the final interactive dashboard and charts[cite: 10, 11].
*   **DAX (Data Analysis Expressions):** Used inside Power BI to calculate custom business metrics[cite: 10].

## Project Workflow
1.  **Data Loading & Cleaning:** I combined both datasets and removed rows that were missing critical information, like price or location[cite: 11, 12]. I also filled in missing review numbers with zeros[cite: 12].
2.  **Feature Engineering:** I created new categories to make the data easier to analyze. For example, I grouped prices into "Budget" or "Luxury," and categorized hosts as "Casual" (1-2 listings) or "Commercial" (3+ listings)[cite: 12].
3.  **Visualization:** I imported the cleaned data into Power BI and designed a four-page interactive report (Overview, Property, Pricing, Host)[cite: 11, 13].
4.  **Interpretation:** I analyzed the visual trends to write business recommendations based purely on what the data showed[cite: 11, 16].

## Key Analysis and Findings
*   **Market Size & Price:** Chicago is the larger market (54.21% of listings) and is more expensive, with an average nightly rate of $310 compared to New Orleans' $275[cite: 10, 13].
*   **Property Preferences:** Guests overwhelmingly prefer private spaces. "Entire Home/Apt" listings make up a massive 77.9% of the market (10,926 units), while shared rooms are almost non-existent[cite: 14, 16].
*   **Host Dominance:** The market is run by professionals, not casual homeowners. "Commercial" hosts (managing 3 or more properties) control the majority of listings in both cities[cite: 15]. The top host manages 173 properties[cite: 16].
*   **Price Elasticity:** Listings priced between $100 and $200 get the most guest reviews (a sign of high bookings). Demand drops sharply for properties priced over $500[cite: 15].

## Visualizations
The Power BI dashboard contains four main sections:
*   **Overview:** High-level metrics showing total listings, market share donuts, and top neighborhoods[cite: 13].
*   **Property Analysis:** Bar charts showing that "Entire Homes" dominate the market and are mostly available year-round[cite: 14].
*   **Pricing Analysis:** A scatter plot that clearly shows how guest demand drops as prices increase, helping identify the perfect "sweet spot" for pricing[cite: 15].
*   **Host Analysis:** Tables and charts revealing how heavily commercial operators dominate the market compared to everyday people renting out their spare rooms[cite: 15].

## Business Insights and Recommendations
*   **Recommendation 1 (Property Type):** Investors should only buy multi-bedroom "Entire Home" properties. Do not invest in properties meant for shared or private room rentals, as they represent a tiny fraction of market demand[cite: 16].
*   **Recommendation 2 (Pricing Strategy):** To get the most bookings, operators should price their entire-home units between $150 and $225 during normal seasons. Pricing too high will significantly hurt occupancy[cite: 16].
*   **Recommendation 3 (Competitive Strategy):** Independent hosts cannot compete with large commercial operators on volume. They should focus on offering unique, hyper-local guest experiences to win good reviews[cite: 17]. 
*   **Recommendation 4 (Regulations):** Hosts should consider setting 3-to-5-night minimum stays during busy weekends to stay compliant with local zoning laws[cite: 17].

## Conclusion
This project successfully transformed raw, messy data from two different cities into a clean, interactive business intelligence tool[cite: 17]. I learned how to use Python for complex data preparation and feature engineering, and I improved my ability to use Power BI to tell a clear, actionable data story[cite: 17]. A well-structured README like this acts as the "reviewer interface" for the project, ensuring the problem, method, and results are easy to inspect.

## How to Run the Project
1. Clone this repository to your local machine.
2. Ensure you have Python installed, along with the `pandas` and `numpy` libraries.
3. Run the `data_preprocessing.py` script to see how the raw data is cleaned and transformed[cite: 18].
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
