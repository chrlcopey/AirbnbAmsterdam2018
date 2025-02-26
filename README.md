# AirbnbAmsterdam2018

# **Airbnb Amsterdam Price Analysis**

## **Introduction**
This project analyzes Airbnb listings in **Amsterdam**, focusing on price variations based on **neighborhoods, property types, seasonality, and other key factors**. Using Python and Tableau, we explore patterns in pricing and availability to gain insights that can help both guests and hosts make informed decisions.

## **Dataset Overview**
The dataset comes from **Inside Airbnb** and provides a snapshot of listings on **December 6th, 2018**. It consists of two main dataframes:

1. **Listings Data (`merged_df`)** - Contains details about **listings**, including price, room type, number of bedrooms, and availability.
2. **Calendar Data (`calendar`)** - Provides **daily availability and pricing** for each listing.

### **Key Columns Used:**
- `neighbourhood` – Location of the listing
- `room_type` – Type of rental (Entire home, Private room, Shared room)
- `price` – Listing price per night (in Euros)
- `bedrooms` – Number of bedrooms per listing
- `availability_365` – Days available per year
- `security_deposit` & `cleaning_fee` – Additional hidden costs
- `reviews_per_month` & `number_of_reviews` – Indicators of listing popularity
- `date` (from `calendar`) – Used to analyze **seasonal price trends**

---

## **Methodology**
1. **Data Cleaning & Preprocessing**:
   - Merged the `listings` and `calendar` datasets using `listing_id`.
   - Converted the `date` column to a `datetime` format and extracted **months**.
   - Converted **geometry data** to WKT format to facilitate geographic visualization.

2. **Exploratory Data Analysis (EDA)**:
   - **Mapped price distribution** across neighborhoods using Tableau.
   - **Computed correlations** between price, bedrooms, availability, and reviews.
   - **Analyzed seasonal trends** in Airbnb pricing.

3. **Findings & Insights**:
   - **The closer a listing is to Amsterdam’s city center, the more expensive it is.**
   - **Prices between neighborhoods can double**, showing significant price disparities.
   - **Room type and property type also influence price**, not just location.
   - **Security deposits and cleaning fees tend to be 2-3 times higher** for high-priced listings.
   - **Listings with more reviews tend to remain popular over time.**
   - **More expensive listings tend to have higher cleaning fees, but the relationship is not strong.**
   - **Seasonal trends show that prices increase in July-September and drop in December-February.**

---

## **Limitations of the Data**
1. **Snapshot in Time** - The dataset is from December 2018 and does not reflect recent pricing trends or market changes.
2. **No Guest Data** - The dataset lacks demographic information about guests, which could provide insights into traveler preferences.
3. **Missing Data** - Some variables, like `host_is_superhost`, have missing values.
4. **Hidden Fees & Discounts** - The dataset does not include **service fees, extra guest charges, or discounts**.
5. **Booking Demand Data Missing** - While we analyze reviews, we don’t have **actual occupancy rates**, making it harder to measure real demand.

---

## **Next Steps & Further Analysis**
- **Explore recent Airbnb datasets** to analyze price trends over time.
- **Deeper seasonal analysis** to see how prices fluctuate across different months and holidays.
- **Investigate Superhost listings** to determine if they charge higher prices or have better occupancy rates.
- **Apply machine learning models** to predict listing prices based on neighborhood, amenities, and availability.
- **Analyze guest preferences** if additional data is available.

---

## **Repository Structure**
```
📂 Airbnb-Amsterdam-Analysis
 ├── 📄 README.md             # Project overview & instructions
 ├── 📂 data                  # Raw & processed datasets
 ├── 📂 notebooks             # Jupyter notebooks for data analysis
 ├── 📂 visualizations        # Tableau dashboards & charts
 ├── 📄 Airbnb_Analysis.ipynb # Main analysis script
 ├── 📄 conclusions.md        # Summary of key findings
```

