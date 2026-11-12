# 🚕 Taxi Fare & Ride Operations Analysis (Power BI)

An end-to-end Business Intelligence solution analyzing **148.77K taxi bookings** across 2024 to uncover revenue drivers, vehicle fleet performance, payment trends, peak-hour demand, and cancellation bottlenecks.

---

## 📊 Key Metrics & Executive Summary
* **Total Bookings:** 148.77K[span_4](start_span)[span_4](end_span)
* **Completed Rides:** 92.55K (~62% completion rate)[span_5](start_span)[span_5](end_span)[span_6](start_span)[span_6](end_span)
* **Cancelled Rides:** 37.43K (~25% overall cancellation rate across driver & customer cancellations)[span_7](start_span)[span_7](end_span)
* **Customer Retention Rate:** 30.12%[span_8](start_span)[span_8](end_span)
* **Service Quality Score:** 77.05[span_9](start_span)[span_9](end_span)

---

## 🛠️ Tech Stack & Data Engineering
* **Power Query (ETL):** Cleaned raw trip logs, handled missing values, standardized date/time formats, and removed anomalies.
* **Data Modeling & Feature Engineering:** Created custom calculated columns and DAX measures to segment operations:
  * `Revenue_Tier` (Low, Medium, High, Premium)[span_10](start_span)[span_10](end_span)
  * `Revenue_per_KM`[span_11](start_span)[span_11](end_span)
  * `Distance_Category` (Short: 0–5 km, Medium: 5–15 km, Long: 15–30 km, Extra Long: 30+ km)[span_12](start_span)[span_12](end_span)
  * `Day_Part` (Morning, Afternoon, Evening, Night) & `Is_Peak_Hour`[span_13](start_span)[span_13](end_span)
  * `Payment_Category` (Digital/UPI, Card, Cash, Wallet)[span_14](start_span)[span_14](end_span)[span_15](start_span)[span_15](end_span)
  * `Driver_Performance_Category` & `Customer_Segment`
  * `Days_Since_Last_Ride` (for retention tracking)

---

## 🔍 Key Business Insights
1. **Fleet Revenue Dominance:** **Auto** leads total booking value (₹13M; 601.79K km travelled)[span_16](start_span)[span_16](end_span), followed by **Go Mini** (₹10M) and **Go Sedan** (₹9M)[span_17](start_span)[span_17](end_span). **Uber XL** generates the lowest volume (₹2M)[span_18](start_span)[span_18](end_span).
2. **Digital Payment Adoption:** **UPI** is the dominant payment mode (generating over ₹20M in booking value), significantly outperforming Cash (~₹13M) and Wallets/Cards[span_19](start_span)[span_19](end_span).
3. **Revenue Concentration:** The **Premium** and **High** revenue tiers account for the vast majority of total booking value, with **Medium (5–15 km)** and **Short (0–5 km)** rides driving the highest revenue per kilometer[span_20](start_span)[span_20](end_span).
4. **Cancellation Bottlenecks:** Out of 37.43K cancellations, customer cancellations stem primarily from *driver delays, AC issues, and plan changes*, while driver cancellations are evenly split across *customer-related issues, excess passengers, and vehicle/personal reasons*[span_21](start_span)[span_21](end_span).

---

## 💡 Actionable Recommendations
* **Incentivize Peak-Hour & Short-Distance Supply:** Increase driver availability during Evening/Night peak windows and high-yield 0–15 km zones where `Revenue_per_KM` is highest[span_22](start_span)[span_22](end_span).
* **Reduce Driver-Induced Cancellations:** Introduce stricter penalties or dispatch alerts when drivers remain stationary post-acceptance to curb "Driver not moving" and "Driver asked to cancel" drops[span_23](start_span)[span_23](end_span).
* **Targeted Retention Campaigns:** Use the `Days_Since_Last_Ride` and `Customer_Segment` metrics to trigger automated UPI cashback offers for dormant riders.

---

## 📁 Dashboard Pages
1. **Home Page:** Interactive navigation menu (`Trends`, `Trips & Routes`, `Payment Analysis`, `About`)[span_24](start_span)[span_24](end_span).
2. **Overall Dashboard:** High-level KPIs, monthly booking trends, and booking status breakdown[span_25](start_span)[span_25](end_span).
3. **Vehicle Type Analysis:** Comparison across Auto, Bike, eBike, Go Mini, Go Sedan, Premier Sedan, and Uber XL[span_26](start_span)[span_26](end_span).
4. **Revenue Analysis:** Payment method splits, daily ride distance trends, and fare distributions[span_27](start_span)[span_27](end_span).
5. **Cancellation Analysis:** Root-cause breakdown of customer vs. driver cancellations[span_28](start_span)[span_28](end_span).
6. **Ratings Dashboard:** Customer vs. driver rating comparisons across vehicle categories[span_29](start_span)[span_29](end_span).
7. **Executive Summary:** Granular KPI tracking (`Service Quality Score`, `Retention Rate`, `Revenue_Tier`, and `Day_Part` trends)[span_30](start_span)[span_30](end_span).
