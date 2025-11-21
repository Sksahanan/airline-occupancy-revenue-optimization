# Airline Occupancy & Revenue Optimization Analysis ✈️

**Repo:** `airline-occupancy-revenue-optimization`  
**Role:** Project Manager & Data Analyst  
**Tech Stack:** Python, Jupyter Notebook, SQLite, pandas, matplotlib / seaborn

---

## 1. Project Overview

This project analyzes an airline’s operational and revenue data to answer a key question:

> **How can we increase aircraft occupancy and optimize pricing to improve overall profitability under rising costs?**

The airline operates a **diverse fleet** (from small business jets to medium-sized aircraft) and faces challenges such as stricter environmental regulations, higher flight taxes, rising fuel prices, and a tight labor market that increases labor costs.  
To protect margins, the focus is on **increasing occupancy rate** and **optimizing fare strategy** to boost **profit per seat**. :contentReference[oaicite:3]{index=3}

---

## 2. Business Problem & Objectives

### 2.1 Business Challenges

- **Stricter environmental regulations** → higher compliance and operating costs.  
- **Higher flight taxes** → more expensive tickets, potential demand drop.  
- **Rising fuel & labor costs** → profitability under pressure.  
- **Need to increase occupancy** on low-performing flights to maximize revenue per seat. :contentReference[oaicite:4]{index=4}  

### 2.2 Project Objectives

1. **Increase occupancy rate** across aircraft and routes.  
2. **Improve pricing strategy** by understanding how fare conditions and aircraft types influence demand.  
3. **Enhance revenue visibility** via KPIs: revenue per ticket, total revenue per aircraft, and occupancy rate per aircraft. :contentReference[oaicite:5]{index=5}  
4. **Simulate a +10% occupancy scenario** to estimate the potential uplift in annual revenue and support strategic decisions. :contentReference[oaicite:6]{index=6}  

---

## 3. Dataset & Tools

### 3.1 Data Sources

- **`travel.sqlite`** – SQLite database containing:
  - Flight / ticket bookings over a summer period (June–August).
  - Aircraft details (aircraft code, total seats).
  - Fare conditions (Business / Economy / Comfort).
  - Ticket price and booking information.

- **Time Window**: Bookings between **2017-06-22 and 2017-08-15** (as seen in booking & revenue trends). :contentReference[oaicite:7]{index=7}  

### 3.2 Tools & Libraries

- **Python** (3.x)
- **Jupyter Notebook**
- **SQLite** (`sqlite3` or `SQLAlchemy`)
- **pandas** – data wrangling  
- **matplotlib / seaborn** – visualizations  
- **NumPy** – numerical operations

---

## 4. Project Structure

```text
.
├── Data Analysis -Airlines.ipynb    # Main analysis notebook (EDA, queries, visuals)
├── travel.sqlite                    # Airline bookings & aircraft data
├── Report (Airlines).pdf           # Business-style summary report with charts
└── README.md                        # Project documentation
```
## 5. Key Analyses & Insights

### 5.1 Aircraft Capacity & Fleet View

- Identified aircraft with **> 100 seats**, including codes such as 319, 320, 321, 733, 763, 773, and SU9.  
- Created a comparison view of **aircraft code vs. seat capacity** as the base for occupancy and revenue-per-seat analysis.  

---

### 5.2 Booking & Revenue Trend Over Time

- Plotted **daily number of tickets** (booking trend) and **daily revenue** to identify demand patterns.  
- Observed:
  - Gradual rise in bookings from late June to early July.  
  - A peak period with the **highest single-day bookings and revenue**.  
  - Stabilization in demand toward mid-August.  

These patterns help identify **high-demand windows** for targeted promotions and pricing adjustments.

---

### 5.3 Fare Conditions & Pricing Strategy

- Compared **average fare per aircraft** across fare conditions:
  - **Business**  
  - **Economy**  
  - **Comfort** (available only on aircraft 773).  
- Key findings:
  - Business class is consistently priced higher than Economy across aircraft.  
  - Some aircraft (e.g., CN1, CR2) only offer Economy → more budget-oriented configuration.  
  - SU9 shows **lower fares but high total revenue**, indicating a **volume-driven profitability** model.  

---

### 5.4 Occupancy Rate per Aircraft

- Calculated **occupancy rate** per aircraft as:  
  `occupancy_rate = booked_seats / total_seats`  
- Derived **average booked seats vs. total seats** for each aircraft.  
- Insight: Higher occupancy → fewer empty seats → better **revenue per flight**, given largely fixed operating costs.

---

### 5.5 Revenue & 10% Occupancy Uplift Scenario

- For each aircraft, measured:
  - **Total revenue**  
  - **Total tickets sold**  
  - **Average revenue per ticket**  
- Simulated a **+10% occupancy uplift** across aircraft to estimate potential revenue gains:
  - Showed a clear **increase in total revenue** as occupancy improves.  
  - Demonstrated how small improvements in **seat utilization** can significantly impact overall profitability.  

---

### 5.6 Business Impact Summary

- The analysis links **operational metrics** (seats, occupancy, aircraft type) with **financial outcomes** (revenue, average fare).  
- Supports decisions on:
  - **Pricing strategy** (e.g., adjusting Business vs. Economy fares).  
  - **Capacity planning** (which aircraft to promote or re-deploy).  
  - **Targeted campaigns** in high-demand periods revealed by booking trends.  
- Overall, the project provides a **data-driven framework** to improve **profit per seat** under rising fuel, tax, and labor costs.

---

## 6. How to Run the Project Locally

### 6.1 Clone the Repository

    git clone https://github.com/<your-username>/airline-occupancy-revenue-optimization.git
    cd airline-occupancy-revenue-optimization

---

### 6.2 (Optional) Create a Virtual Environment

    python -m venv venv

On macOS / Linux:

    source venv/bin/activate

On Windows:

    venv\Scripts\activate

---

### 6.3 Install Dependencies

Create a `requirements.txt` file in the project root with:

    pandas
    numpy
    matplotlib
    seaborn
    jupyter
    sqlalchemy

Then install all dependencies:

    pip install -r requirements.txt

---

### 6.4 Launch Jupyter Notebook

    jupyter notebook

- Open `Data Analysis -Airlines.ipynb`.  
- Ensure `travel.sqlite` is in the **same folder** as the notebook.  
- Run all cells in order to reproduce the analysis, visualizations, and insights.

---

## 7. Usage Ideas

Once the notebook is running, you can:

- Explore **aircraft-wise occupancy** and identify **low-performing aircraft or routes**.  
- Experiment with **pricing strategies** by adjusting fare assumptions and re-running revenue/occupancy calculations.  
- Extend the analysis to:
  - Forecast future bookings using basic time-series methods.  
  - Build a prototype **dynamic pricing** or **seat inventory optimization** experiment.  
  - Segment customers by **fare class** and **booking behavior** for more targeted offers and promotions.  

This makes the project a strong base for both **operations** and **revenue management** use cases.

---

## 8. Future Enhancements

- Add **predictive models** (e.g., regression, ARIMA, tree-based models) to forecast demand and load factors.  
- Include **route-level profitability**, not just aircraft-level analysis.  
- Build an interactive **dashboard** (Streamlit / Power BI / Dash) for revenue managers to explore KPIs in real time.  
- Incorporate external factors such as **seasonality, public holidays, fuel prices, and taxes** into the analysis and scenarios.  
- Integrate **what-if simulators** for pricing, discount levels, capacity changes, and aircraft reassignment.  

---

## 9. Resume-Ready Highlights (Project Manager / Data Analytics)

You can use these bullets directly in your resume or LinkedIn:

- Led an end-to-end airline analytics project across **7 aircraft types and 3 fare classes**, using **Python, SQLite, and Jupyter** to analyze occupancy, pricing, and key revenue drivers.  
- Defined and tracked **core KPIs** – revenue per ticket, occupancy rate per aircraft, and total revenue – and ran a **+10% occupancy uplift scenario** to estimate financial upside and support decision-making.  
- Translated insights into **pricing and capacity recommendations** (e.g., tightening fares on high-demand SU9 routes vs. improving CN1 utilization) to help navigate rising environmental, tax, and labor costs while protecting profitability.  

---

## 10. License

MIT License – feel free to use, adapt, and extend this project with attribution.
