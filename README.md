#  BART Data Analytics & Data Science Project

##  Overview
This project analyzes San Francisco BART (Bay Area Rapid Transit) ridership data from 2016 and 2017 to discover passenger travel patterns, identify peak hours, compute station distances, and propose machine learning approaches for commuting volume prediction.

---

##  Data Preparation
* Merged ridership datasets for **2016** and **2017**.
* Joined station metadata (`station_info.csv`) to map station names and geographical coordinates (`Latitude` & `Longitude`).
* Extracted date and time features (hour of the day, day of the week) for time-based analysis.

---

##  Data Analytics Questions & Findings

1. **Which BART station is the busiest?**
   * Identified top stations based on total incoming (`Origin`) and outgoing (`Destination`) passengers.

2. **What is the least popular BART route?**
   * Ranked Origin-Destination station pairs to find the least traveled routes.

3. **When is the best time to go to SF from Berkeley if you want to find a seat?**
   * Analyzed hourly travel volume from Berkeley stations to SF stations to find off-peak hours with minimum crowd.

4. **Which day of the week is the busiest?**
   * Aggregated total throughput across days of the week to find peak travel days.

5. **How many people take the BART late at night?**
   * Calculated total passenger volume between 22:00 and 05:00.

---

##  Data Science Questions

### A. Distance Calculation
* Calculated straight-line distances between stations using coordinate-based distance estimation (Pythagorean distance).

### B. Predictive Model Approach
* **Goal:** Predict commuting volume between any 2 stations.
* **Model Approach:** Regression / Time-Series model (e.g., Random Forest or XGBoost) trained on historical hourly patterns.
* **Additional Data Needed:** Weather conditions, public holidays/events, city road traffic, and fuel prices.
* **Use Cases for BART Officials:**
  * Optimize train schedules and capacity during peak vs. off-peak hours.
  * Plan maintenance during low-traffic time slots.
  * Improve station staffing and security management.

---

##  Tech Stack
* **Language:** Python
* **Libraries:** `pandas`, `math`
* **Environment:** Jupyter Notebook

---

##  Conclusion
By analyzing travel times, popular routes, and station distances, this project provides data-backed insights to improve BART train scheduling, operational efficiency, and overall passenger experience.
