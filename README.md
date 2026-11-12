# 🚕 Taxi Fare & Ride Operations Analysis (Power BI)

An end-to-end Business Intelligence solution analyzing **148.77K taxi bookings** across 2024 to uncover revenue drivers, vehicle fleet performance, payment trends, peak-hour demand, and cancellation bottlenecks.

---

## 📊 Key Metrics & Executive Summary
* **Total Bookings:** 148.77K
* **Completed Rides:** 92.55K (~62% completion rate)
* **Cancelled Rides:** 37.43K (~25% overall cancellation rate across driver & customer cancellations)
* **Customer Retention Rate:** 30.12%
* **Service Quality Score:** 77.05

---

## 🛠️ Tech Stack & Data Engineering
* **Power Query (ETL):** Cleaned raw trip logs, handled missing values, standardized date/time formats, and removed anomalies.
* **Data Modeling & Feature Engineering:** Created custom calculated columns and DAX measures to segment operations:
  * `Revenue_Tier` (Low, Medium, High, Premium)
  * `Revenue_per_KM`
  * `Distance_Category` (Short: 0–5 km, Medium: 5–15 km, Long: 15–30 km, Extra Long: 30+ km)
  * `Day_Part` (Morning, Afternoon, Evening, Night) & `Is_Peak_Hour`
  * `Payment_Category` (Digital/UPI, Card, Cash, Wallet)
  * `Driver_Performance_Category` & `Customer_Segment`
  * `Days_Since_Last_Ride` (for retention tracking)

---

## 🔍 Key Business Insights
1. **Fleet Revenue Dominance:** **Auto** leads total booking value (₹13M; 601.79K km travelled), followed by **Go Mini** (₹10M) and **Go Sedan** (₹9M). **Uber XL** generates the lowest volume (₹2M).
2. **Digital Payment Adoption:** **UPI** is the dominant payment mode (generating over ₹20M in booking value), significantly outperforming Cash (~₹13M) and Wallets/Cards.
3. **Revenue Concentration:** The **Premium** and **High** revenue tiers account for the vast majority of total booking value, with **Medium (5–15 km)** and **Short (0–5 km)** rides driving the highest revenue per kilometer.
4. **Cancellation Bottlenecks:** Out of 37.43K cancellations, customer cancellations stem primarily from *driver delays, AC issues, and plan changes*, while driver cancellations are evenly split across *customer-related issues, excess passengers, and vehicle/personal reasons*.

---

## 💡 Actionable Recommendations
* **Incentivize Peak-Hour & Short-Distance Supply:** Increase driver availability during Evening/Night peak windows and high-yield 0–15 km zones where `Revenue_per_KM` is highest.
* **Reduce Driver-Induced Cancellations:** Introduce stricter penalties or dispatch alerts when drivers remain stationary post-acceptance to curb "Driver not moving" and "Driver asked to cancel" drops.
* **Targeted Retention Campaigns:** Use the `Days_Since_Last_Ride` and `Customer_Segment` metrics to trigger automated UPI cashback offers for dormant riders.

---

## 📁 Dashboard Pages
1. **Home Page:** Interactive navigation menu (`Trends`, `Trips & Routes`, `Payment Analysis`, `About`).
2. **Overall Dashboard:** High-level KPIs, monthly booking trends, and booking status breakdown.
3. **Vehicle Type Analysis:** Comparison across Auto, Bike, eBike, Go Mini, Go Sedan, Premier Sedan, and Uber XL.
4. **Revenue Analysis:** Payment method splits, daily ride distance trends, and fare distributions.
5. **Cancellation Analysis:** Root-cause breakdown of customer vs. driver cancellations.
6. **Ratings Dashboard:** Customer vs. driver rating comparisons across vehicle categories.
7. **Executive Summary:** Granular KPI tracking (`Service Quality Score`, `Retention Rate`, `Revenue_Tier`, and `Day_Part` trends).
