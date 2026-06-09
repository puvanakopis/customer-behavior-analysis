# 🛒 Superstore — Retail Performance Analysis
### A Complete Exploratory Data Analysis & Business Intelligence Portfolio Project


## 📋 Table of Contents
- [Project Introduction](#-project-introduction)
- [Dataset Overview](#-dataset-overview)
- [Business Objective](#-business-objective)
- [Key Questions Answered](#-key-questions-answered)
- [Project Structure](#-project-structure)
- [Tech Stack](#-tech-stack)
- [How to Run](#-how-to-run)
- [Key Insights](#-key-insights)
- [Recommendations](#-recommendations)
- [Conclusion](#-conclusion)
- [Author](#-author)

<br>

## 📦 Project Introduction

The ** Superstore** dataset is a widely-used retail analytics dataset that captures transactional data from a fictional U.S.-based superstore chain. It contains **9,994 order records** spanning multiple years across four geographic regions.

| Attribute      | Detail                      |
|----------------|-----------------------------|
| **Records**    | 9,994 rows                  |
| **Features**   | 13 columns                  |
| **Domain**     | Retail / E-commerce         |
| **Geography**  | United States (4 Regions)   |

<br>

## 🎯 Business Objective

This analysis aims to uncover actionable intelligence that enables stakeholders to:

- Identify top-performing and under-performing product categories and sub-categories
- Understand the impact of discounting on profitability
- Detect regional and segment-level performance patterns
- Provide data-driven recommendations to improve margins and reduce losses

<br>

## ❓ Key Questions Answered

1. Which **product categories and sub-categories** generate the highest revenue and profit?
2. Which **regions and states** are most and least profitable?
3. How do **discount rates** affect sales and profit margins?
4. Which **customer segments** contribute most to revenue?
5. What are the **shipping mode preferences** and how do they relate to profitability?
6. Are there **seasonal trends** in sales performance?
7. Which **sub-categories are consistently loss-making**?

<br>

## 📁 Project Structure

```text
customer-behavior-analysis/
│
├── .gitignore                # Git ignore rules
├── .python-version           # Python version configuration
├── Superstore.csv            # Raw dataset
├── Superstore_EDA.ipynb      # Complete EDA notebook
├── pyproject.toml            # Project dependencies and metadata
├── uv.lock                   # UV dependency lock file
└── README.md                 # Project documentation
```

<br>

## 🛠️ Tech Stack

| Library        | Purpose                              |
|----------------|--------------------------------------|
| `pandas`       | Data manipulation & aggregation      |
| `numpy`        | Numerical computations               |
| `matplotlib`   | Base plotting & chart customisation  |
| `seaborn`      | Statistical visualisations           |

<br>

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/puvanakopis/customer-behavior-analysis.git
cd customer-behavior-analysis
```

### 2. Install dependencies using UV

```bash
uv sync
```

This will automatically create a virtual environment and install all dependencies from `pyproject.toml`.

### 3. Activate the virtual environment

**Windows (PowerShell)**

```bash
.venv\Scripts\activate
```

**Linux / macOS**

```bash
source .venv/bin/activate
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook Superstore_EDA.ipynb
```

Alternatively:

```bash
jupyter lab
```

### 5. Open the notebook

Open:

```text
Superstore_EDA.ipynb
```

and run all cells.

> **Note:** Ensure `Superstore.csv` is available in the project root directory before running the notebook.

<br>

## 💡 Key Insights

1. **Discounting is the #1 profitability killer.** Orders with discounts above 20% are predominantly loss-making. The negative correlation between discount and profit is the single strongest signal in the dataset.

2. **~28% of all orders generate a net loss.** Nearly one in three transactions destroys value — indicating a systemic pricing or discounting problem that costs the business tens of thousands of dollars annually.

3. **Technology is the star performer.** It leads in both total sales and total profit, with the highest average margin, and maintains profitability even at moderate discounts.

4. **Furniture is a structural profitability problem.** Despite ranking second in sales, its profit contribution is disproportionately low. Tables and Bookcases sub-categories are consistently loss-making.

5. **Office Supplies drives volume, not value.** It accounts for the most orders but has the lowest average order value. Margin management here is critical given scale.

6. **The Central region is the weakest performer.** Despite reasonable order volume, Central delivers the lowest total profit — particularly on Furniture orders.

7. **Texas and Ohio destroy significant value.** These high-revenue states are among the biggest profit destroyers, suggesting heavy discounting or an unfavourable product mix.

8. **California and New York are the profit powerhouses.** Combined, they contribute the majority of positive profit, subsidising loss-making regions.

9. **Same Day shipping is rare but efficient.** It accounts for <5% of orders but delivers competitive profit margins, suggesting it targets higher-value customers.

10. **Standard Class dominates at ~60% of orders.** This creates a cost structure skewed towards slower fulfilment — a potential opportunity for last-mile optimisation.

11. **High-quantity orders don't guarantee high profits.** Orders of 10–14 units often show below-average profit, possibly due to bulk discount arrangements.

12. **The Consumer segment is largest by volume but Home Office is the most margin-efficient** when discounting behaviour is controlled for.

<br>

## 📊 Recommendations

| Priority | Action                              | Potential Impact                        |
|----------|-------------------------------------|-----------------------------------------|
| 1        | Cap all discounts at 20%            | Reduce loss-making orders by ~35%       |
| 2        | Reprice or exit Tables/Bookcases    | Recover ~$80–100K in annual profit      |
| 3        | Focus technology sales in CA/NY     | Accelerate profit growth in core markets|

### Detailed Recommendations

**Rec 1 — Enforce a Strict Discount Cap of 20%**
Implement a system-level approval gate that prevents front-line staff from applying discounts above 20% without senior sign-off. For Furniture specifically, cap at 15%.

**Rec 2 — Exit or Reprice Tables and Bookcases**
Conduct a cost-to-serve analysis. Either renegotiate supplier contracts to restore margin, increase retail pricing by 15–20%, or discontinue and redirect shelf space to higher-margin items (e.g., Copiers, Phones, Accessories).

**Rec 3 — Launch a Central-Region Profitability Recovery Plan**
Appoint a regional profitability manager tasked with auditing discount practices, optimising the product mix toward Technology, and renegotiating logistics contracts.

**Rec 4 — Double Down on Technology in California and New York**
Increase marketing spend and sales headcount in these markets. Introduce loyalty programmes targeting Corporate and Home Office buyers to deepen wallet share.

**Rec 5 — Introduce Dynamic Pricing and Promotion Controls**
Deploy a rules-based pricing engine that dynamically limits discounts based on product margin tier, customer segment, and regional performance.

<br>

## 📝 Conclusion

This analysis of 9,994 Superstore transactions reveals a business generating strong **top-line revenue** (~$2.3M total sales) but facing significant **margin leakage** that suppresses net profitability. The root cause is clearly identifiable: a culture of aggressive discounting that disproportionately impacts the Furniture category and the Central geographic region.

**Technology** emerges as the undisputed profit engine, combining high average order values with resilient margins and strong demand across all regions. By contrast, **Furniture** — particularly Tables and Bookcases — represents value-destroying inventory that warrants urgent strategic review.

With targeted interventions on discounting, product mix, and regional focus, the business has a credible pathway to improving its profit margin from the current ~12% blended average to a target of **18–22%** within 12–18 months — without sacrificing revenue momentum.

<br>

## 👤 Author

**Name:** Puvanakopis  
**GitHub:** [@puvanakopis](https://github.com/puvanakopis)  
**LinkedIn:** [Puvanakopis](https://www.linkedin.com/in/puvanakopis/)  
**Email:** puvanakopis@gamil.com

<br>

*If you found this project useful, feel free to ⭐ star the repository and share your feedback!*
