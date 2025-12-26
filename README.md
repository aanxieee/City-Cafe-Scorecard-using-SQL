# City Cafe Expansion Scorecard (SQL Project)
SQL-based scorecard that turns raw, scattered sales and city data into clean metrics, business-ready insights, and a repeatable framework to decide the **top Indian cities for opening new City Cafe outlets**.

---

## Project Positioning
- **Unmanageable data → clean metrics**: Started with flat CSVs (cities, customers, products, sales) and built a relational schema plus validated metrics in SQL.
- **Clean metrics → business insight**: Designed a scorecard that connects revenue, rent efficiency, population, and coffee consumption to rank cities.
- **Business insight → automation**: Structured queries and views that can be plugged into a dashboard or scheduled refresh for ongoing expansion decisions.

This project shows how I use SQL to move from messy data to a **repeatable decision engine** for location strategy.

---

## Problem Statement
City Cafe is an online coffee brand (since 2023) exploring **which Indian cities should get new physical outlets first**. Leadership wants:

- A **data-backed ranking** of cities instead of gut feeling.
- A view of **demand, spending power, and rent efficiency** together.
- A scalable way to **re-run the analysis** as new data comes in.

The question: **Which top 3 cities offer the best market potential for new City Cafe stores?**

---

## My Solution (Tech + Approach)
**Tech stack**
- SQL (relational modeling, joins, aggregations, window functions).
- Source files: `city.csv`, `customers.csv`, `products.csv`, `sales.csv`.
- Core logic implemented in: `Schemas.sql` (data model) and `Solutions.sql` (business logic queries).

**Approach**
1. **Model the data**  
   - Designed tables for cities, customers, products, and sales.  
   - Linked them via keys so every sale can be traced to a city, customer, and product.

2. **Clean and standardize metrics**  
   - Derived consistent units for revenue, rent, and per-customer KPIs.  
   - Estimated coffee consumers per city (assuming 25% of population consumes coffee).

3. **Build the scorecard in SQL**  
   - Wrote queries to compute city-level metrics: total revenue, total customers, estimated coffee consumers, rent per customer, and average sale per customer.  
   - Calculated monthly sales trends to capture growth and stability.

4. **Rank cities for expansion**  
   - Combined demand (customers, coffee consumers), revenue, and rent efficiency.  
   - Recommended the **top 3 cities** with the strongest overall profile.

5. **Prepare for automation**  
   - Organized logic into reusable SQL scripts that can be turned into **views, stored procedures, or scheduled jobs** in a production database / BI stack.

---

## Business Questions Answered
1. **Coffee consumption potential**  
   - How many people in each city likely consume coffee (assuming 25% of population)?

2. **Revenue performance**  
   - What is the total revenue from coffee sales across all cities in Q4 2023?

3. **Product performance**  
   - How many units of each product were sold, and which products lead by volume and value?

4. **Customer value by city**  
   - What is the average sales amount per customer in each city?

5. **City profile**  
   - What are each city’s population, estimated coffee consumers, and number of unique customers?

6. **Top-selling products by city**  
   - What are the top 3 selling products in each city?

7. **Sales vs. rent efficiency**  
   - What is the average sale per customer vs. average rent per customer for each city?

8. **Growth over time**  
   - How is sales performance changing month over month (growth / decline)?

9. **Market potential & ranking**  
   - Which **top 3 cities** stand out when we consider sales, rent, customers, and estimated coffee consumers together?

---

## Key Insights & Recommendations
Based on the scorecard, the **top 3 recommended cities** for new City Cafe outlets are:

**1. Pune**  
- Very low average rent per customer.  
- Highest total revenue.  
- Strong average sales per customer.

**2. Delhi**  
- Highest estimated coffee consumers (~7.7 million).  
- Very high total number of customers (68).  
- Reasonable average rent per customer (~330, under 500).

**3. Jaipur**  
- Highest number of customers (69).  
- Very low average rent per customer (~156).  
- Healthy average sales per customer (~11.6k).

These cities balance **demand, revenue, and cost efficiency**, making them strong early bets for physical expansion.

---

## From Analysis to Automation
This project is structured so it can be easily scaled:

- Turn the core queries into **database views** for dashboards.  
- Wrap logic into **stored procedures** to refresh the scorecard on new data.  
- Connect to BI tools (Power BI, Tableau, etc.) to give leadership a live **expansion decision dashboard**.

---

## Author
Project by **Aanya Mittal** .  
Portfolio: [aanxiee.com](https://www.aanxiee.com/)
