# AtliQ Power-BI_Business_Insight_360
AtliQ Business Insights 360
A cross‑functional Power BI initiative for smarter, faster decisions

 # Project Snapshot
AtliQ Hardware has expanded worldwide but recently suffered a costly mis‑step in the U.S. market. To stay competitive against rivals who already rely on data science, the company launched its first enterprise‑wide analytics program. Business Insights 360 delivers a suite of Power BI dashboards that translate raw operational data into actionable insights for Finance, Sales, Marketing, Supply Chain and the Executive team.

![Image](https://github.com/user-attachments/assets/185075ab-6aaf-4c25-8849-0fb3f1a1da65)
# Live Dashboard Link:
 https://app.powerbi.com/view?r=eyJrIjoiNGU4MWU0MjMtY2Q5OC00OTU2LWI5NjktNWFkZjBiOTUzNmFiIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9
# Tech Stack
| Core                            | Supporting                         |
|---------------------------------|------------------------------------|
| Power BI Desktop & Service      | SQL, Excel                         |
| DAX, M                          | DAX Studio (optimization)          |
| Personal data gateway (auto-refresh) | Project charter & documentation |
# Power BI Techniques Learned

- Creating **calculated columns** and **DAX measures**
- Using **KPI indicators**, conditional formatting (icons/colors)
- **Bookmarks** and button-based **page navigation**
- Creating a **date table** using **M language**
- Using **dynamic titles** (based on filters)
- Data **validation techniques**
- Tooltips for detailed data without using extra space
- Avoiding divide-by-zero errors using `DIVIDE()` function
- Publishing reports to **Power BI Service**
- Setting up **Personal Gateway** for **auto-refresh**
- Creating and managing **Power BI Apps**
- Controlling **access permissions** and workspaces
- Optimizing file size using **DAX Studio**
# Soft Skills Developed

- Stakeholder mapping and communication
- Conducting project kickoff sessions and requirement gathering
- Understanding domain knowledge in:
  - Sales
  - Finance
  - Marketing
  - Supply Chain
# Business Terms Glossary

- **Gross Margin**, **Gross Margin %**
- **Gross Sales**, **Gross Sales %**
- **Pre-invoice deductions**, **Post-invoice deductions**
- **Net Sales**, **Net Invoice Sales**
- **Net Profit**, **Net Profit %**
- **COGS** – Cost of Goods Sold
- **YTD** – Year to Date
- **YTG** – Year to Go
- **Sales Channels**: Direct, Retailer, Consumer, Distributor
# Company Background  
- **Name**: AtliQ Hardware  
- **Industry**: Computer systems & accessories  
- **Sales Channels**: Retailer, Direct, Distributor  
- **Markets**: 27 countries, 4 major regions (APAC, EU, LATAM, Others)

The company previously relied on surveys and Excel for decision-making. A failed retail expansion
#  Discovery Questions (Before Dashboard Build)

1. What is the objective of this dashboard?
2. How will project success be measured?
3. What is the deadline?
4. Are stakeholders expecting a preview/demo?
5. What do stakeholders hope to achieve?
6. What fears or concerns do they have?
7. Who will use the dashboard? For what purpose?
8. What are stakeholders' design expectations?
9. What can go wrong?
10. What data/resources are needed?
11. Any input on layout/views from stakeholders?
# Dataset Understanding

### 🔹 Dimension Tables
- `dim_customer`: 75 customers, 27 markets, 2 platforms (Brick & Mortar, E-commerce)
- `dim_market`: 7 sub-zones, 4 regions
- `dim_product`: Divisions (P&A, N&S), 14 categories, product variants

### 🔹 Fact Tables
- `fact_forecast_monthly`: Monthly forecasted demand data (denormalized)
- `fact_sales_monthly`: Monthly actual sold quantities

### 🔹 Additional Tables
- `freight_cost`: Market-wise travel & transport cost
- `gross_price`: Product-wise gross price
- `manufacturing_cost`: Product/year-wise cost data
- `pre_invoice_deductions`: Customer-wise deduction % before invoice
- `post_invoice_deductions`: Post-sale deductions data

All monthly data is aligned to the **start of each month** for aggregation purposes
# Data Modeling  
- **Approach**: Snowflake schema  
- **Why**: Better performance, separation of dimensions and facts  
- **Focus**: 
  - Clean relationships (1-directional)
  - Avoid circular dependency
  - Proper surrogate keys

> Poor data modeling impacts performance. We followed best practices to ensure smooth interactivity
<img width="720" alt="Image" src="https://github.com/user-attachments/assets/536ad76a-8c14-46f1-bf59-068cd6fca2f9" />

# Dashboard Views

| View             | Description |
|------------------|-------------|
| **Home**         | Navigation hub to all dashboards |
| **Finance**      | Budgeting, cost control, forecasting |
| **Sales**        | Product/customer trends, unit economics |
| **Supply Chain** | Demand accuracy, lead times, supplier metrics |
| **Marketing**    | Campaign KPIs, product-market performance |
| **Executive**    | Enterprise-wide performance view |
| **Info / Support** | Project context, terms, user help |
# Goals & Key Wins by Perspective

---
# 🏠 Home View

**Overview:**
- Acts as the navigation hub for all report sections  
- Buttons direct users to each view: Finance, Sales, Marketing, Supply Chain, Executive, etc.  
- Includes quick access to Info and Support pages
![Image](https://github.com/user-attachments/assets/5a89129a-c53f-4614-92fa-70ed055487db)
### # 💰 Finance View

**Objectives:**
- Improve financial planning and budgeting processes  
- Enhance cost control and expense management

**Key Achievements:**
- Built a robust financial forecasting model, improving budget accuracy  
- Benchmarked budgets against previous year and targets
![Image](https://github.com/user-attachments/assets/ab6c7608-37d5-4b69-bd6b-dd90d3eaef68)
# 📈 Sales View

**Objectives:**
- Increase sales revenue and market share  
- Improve customer relationship management

**Key Achievements:**
- Created product/customer-wise sales performance and unit economics reports  
- Tracked sales trends and key sales KPIs
![Image](https://github.com/user-attachments/assets/21d59048-90b7-4d4f-8702-c026f3edaecf)
# 📢 Marketing View

**Objectives:**
- Increase brand visibility and customer engagement  
- Implement data-driven marketing strategies

**Key Achievements:**
- Built region- and product-wise market performance reports with unit economics  
- Identified marketing trends and tracked campaign KPIs
![Image](https://github.com/user-attachments/assets/48b6b116-2af9-4785-a0bb-5f19c69de45d)
# 🏭 Supply Chain View

**Objectives:**
- Optimize inventory management and reduce lead times  
- Enhance supplier relationships for cost savings

**Key Achievements:**
- Identified trends in forecast accuracy %, net error %, and absolute error %  
- Built key supply metrics by customer and product
![Image](https://github.com/user-attachments/assets/8744dd1f-24b0-4198-9ca1-53db65ab84de)
# 🧠 Executive View

**Objectives:**
- Provide a complete organizational performance overview  
- Enable data-driven decision-making for leadership

**Key Achievements:**
- Developed an executive dashboard for real-time performance monitoring  
- Visualized revenue by division, product, customer, and channel using ribbon and bar charts
![Image](https://github.com/user-attachments/assets/12d58578-14e8-453b-b3bb-57e5d6cc3224)
# Live Dashboard Preview
https://github.com/user-attachments/assets/91072a2c-10ef-4465-bbe2-1ff30be23cbd
# Project Outcome

- Enabled **data-driven decisions** across departments
- Improved **forecasting accuracy** and reduced warehousing cost
- **Sales teams** now focus on high-profit customers and products
- Boosted internal **data literacy** and analytical mindset
- Answered key "why" questions across business functions
![Image](https://github.com/user-attachments/assets/894971de-66e8-4dee-85a2-a68fc0451cc4)
![Image](https://github.com/user-attachments/assets/2738821f-f664-498a-9efd-697506c491b7)
# Conclusion

**Business Insights 360** transformed AtliQ's decision-making process. By integrating data from Finance, Sales, Marketing, Supply Chain, and Executive functions into an intelligent Power BI system, AtliQ now navigates its global operations with confidence, clarity, and data at its core.
