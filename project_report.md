# 📊 Project Report: Airbnb Market Dynamics (Chicago vs. New Orleans)

**Category:** Data Analytics Portfolio Project  
**Tools Used:** Python, Pandas, NumPy, Power BI  

---

## 1. Executive Summary
This project analyzes short-term rental market dynamics by comparing Airbnb listings in Chicago and New Orleans. Utilizing Python for robust data preparation and Power BI for interactive visualization, the analysis processed an integrated dataset of 14,021 active listings. Key findings reveal that Chicago represents a slightly larger market share (54.21%) and commands higher average nightly rates ($310 vs. $275). Both markets are dominated by "Entire Home/Apt" listings and commercial hosts operating three or more properties. These insights provide actionable intelligence for hosts optimizing pricing strategies and investors evaluating market entry.

## 2. Introduction
The short-term rental marketplace, spearheaded by platforms like Airbnb, has transformed urban hospitality. Comparing listing dynamics across diverse cities provides critical insights into regional demand and pricing elasticity. Chicago, a major northern metropolitan business hub, and New Orleans, a southern cultural and tourist epicenter, offer a compelling comparative study of urban short-term rental behavior.

## 3. Problem Statement
Prospective hosts and real estate investors often lack synthesized data to make informed market entry and pricing decisions. By comparing pricing structures, property types, availability trends, neighborhood distribution, and host behaviors between Chicago and New Orleans, this project aims to uncover the underlying market forces. Understanding these dynamics is essential for optimizing listing performance, anticipating market saturation, and maximizing occupancy.

## 4. Project Objectives
* **Data Preparation:** Clean, standardize, and engineer a combined dataset using Python.
* **Market Comparison:** Evaluate listing volume and average pricing across cities.
* **Property Distribution:** Analyze the composition of room types and availability.
* **Host Segmentation:** Assess the influence of commercial versus casual hosting.
* **Business Insights:** Deliver actionable recommendations via an interactive Power BI dashboard.

## 5. Dataset Description
The analysis is based on two raw CSV datasets containing listing-level Airbnb data for Chicago and New Orleans. Upon ingestion, integration, and cleaning, the final consolidated dataset comprises 14,021 valid records (7,601 for Chicago; 6,420 for New Orleans).

| Variable | Data Type | Description |
| :--- | :--- | :--- |
| `id` | Numeric | Unique identifier for the Airbnb listing. |
| `price` | Numeric | Stated nightly rate in USD. |
| `room_type` | Categorical | Type of space (Entire home, Private room, etc.). |
| `availability_365` | Numeric | Days available for booking over the next year. |
| `host_id` / `host_name` | Numeric / Text | Identifiers for the property host. |
| `number_of_reviews` | Numeric | Total reviews, serving as a proxy for engagement. |

## 6. Tools and Technologies
* **Python (Pandas, NumPy):** Utilized for data ingestion, missing value treatment, text standardization, and complex feature engineering (e.g., categorizing price tiers and host behavior).
* **Power BI:** Employed to develop a four-page interactive dashboard, utilizing DAX for aggregations and diverse visuals to communicate findings.

## 7. Data Cleaning and Preprocessing
Robust data hygiene is foundational to accurate analysis. The following operations were executed via Python:
* **Critical Null Removal:** Rows missing `price`, `latitude`, `longitude`, or `host_id` were dropped, as they lack core operational utility.
* **Column Pruning:** The `neighbourhood_group` column was entirely empty and subsequently dropped to reduce dimensionality.
* **Imputation:** Missing `reviews_per_month` were filled with 0, and `last_review` with "No Reviews".
* **Deduplication:** Duplicate rows based on listing `id` were removed to prevent double-counting.

## 8. Feature Engineering
To facilitate aggregate analysis in Power BI, continuous and granular variables were transformed into categorical tiers:
* **price_tier:** Segmented into Budget (<$75), Standard ($75-$200), Premium ($201-$500), and Luxury (>$500) to allow investors to analyze distinct market segments.
* **host_type:** Created by counting total listings per `host_id`. Classified as Commercial (3+ listings) or Casual (1-2 listings) to identify the professionalization of the local market.
* **availability_tier:** Segmented into Fully Booked/Inactive (0), Low (<90 days), Medium (<270), and High (>270).
* **engagement_tier:** Categorized based on `number_of_reviews` (None, Low, Moderate, High).

## 9. Exploratory Data Analysis & Key Findings
The comparative analysis surfaced distinct operational realities between the two cities. 

| Business Question | Chicago Result | New Orleans Result | Business Implication |
| :--- | :--- | :--- | :--- |
| **Market Volume** | 7.6K listings (54.2%) | 6.4K listings (45.8%) | Chicago represents a slightly larger volume, but NOLA is highly dense relative to city size. |
| **Pricing** | $310 Avg. Rate | $275 Avg. Rate | Chicago commands a ~12% pricing premium on average. |
| **Property Type** | 5,813 Entire Homes | 5,113 Entire Homes | Entire properties completely dominate both markets; shared rooms are negligible. |
| **Host Professionalism** | 4.4K Commercial listings | 3.7K Commercial listings | The majority of inventory is managed by professional, multi-listing entities in both cities. |
| **Top Neighborhoods** | Near North Side, Loop | Central Business Dist. | Pricing power is heavily concentrated in downtown/business districts. |

## 10. Power BI Dashboard Analysis
The interactive dashboard comprises four thematic pages designed for stakeholder decision-making:
* **Page 1 — Overview:** Establishes the macro environment. It highlights the 14.021K total listings and a combined average rate of $294.40. 
* **Page 2 — Property Analysis:** Focuses on inventory composition. The Room Type Inventory Matrix proves that "Entire Home/Apt" (10,926 units combined) is the definitive industry standard.
* **Page 3 — Pricing Analysis:** Explores revenue dynamics. The Price Tier Breakdown confirms that "Standard" and "Premium" tiers hold the vast majority of volume. 
* **Page 4 — Host Analysis:** Evaluates operator behavior. The Casual vs. Commercial bar chart reveals that commercial hosts control the majority of inventory. The Top Hosts matrix shows operators managing massive portfolios (e.g., 173 listings).

## 11. Business Recommendations
* **For Investors:** Focus acquisitions on "Entire Home/Apt" properties in central districts (e.g., Chicago's Loop, NOLA's Central Business District). The data proves this format captures the vast majority of market demand.
* **For Hosts:** Optimize pricing within the "Standard" to "Premium" bands ($150–$300). The price-to-review scatter plot clearly shows engagement drops drastically for properties priced above $400/night outside of boutique hotel categories.
* **Market Strategy:** Casual hosts must recognize they are competing against highly professionalized commercial entities. Competing on unique local experiences or distinct interior design is crucial when competing with commercial scale.

## 12. Conclusion
This comparative analysis successfully mapped the short-term rental landscapes of Chicago and New Orleans. By leveraging Python for data wrangling and Power BI for visualization, the project uncovered that both markets are highly professionalized and dominated by entire-home listings. While Chicago offers a larger volume and higher average rates, both cities exhibit similar structural characteristics regarding commercial host dominance and price-tier distribution.