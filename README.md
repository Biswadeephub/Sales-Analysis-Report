#  Retail Sales Analysis

An exploratory data analysis (EDA) project that examines **9,994 retail transactions** from a US-based superstore to uncover sales trends, profitability drivers, and actionable business insights using **Python**, **Pandas**, **NumPy**, and **Matplotlib**.

---

##  Objective

Identify patterns across regions, product categories, sub-categories, cities, and discount strategies to answer key business questions:

- Which **regions and cities** drive the most revenue?
- Which **product categories** are most profitable — and which are loss-makers?
- How do **discounts** impact profitability?
- What **actionable recommendations** can be derived from the data?

---

##  Project Structure

```
Retail-Sales-Analysis/
├── Data/
│   └── SampleSuperstore.csv   # Source dataset (9,994 rows × 13 columns)
├── images/                     # Exported visualizations / screenshots
├── Sales_analysis.ipynb        # Jupyter Notebook with full analysis
└── README.md
```

---

##  Dataset Overview

| Column | Type | Description |
|---|---|---|
| Ship Mode | str | Shipping method (Standard, Second Class, etc.) |
| Segment | str | Customer segment (Consumer, Corporate, Home Office) |
| Country | str | Country of sale (United States) |
| City | str | City of the customer |
| State | str | State of the customer |
| Postal Code | int | Postal code |
| Region | str | Geographic region (West, East, Central, South) |
| Category | str | Product category (Technology, Furniture, Office Supplies) |
| Sub-Category | str | Product sub-category (17 unique values) |
| Sales | float | Revenue from the transaction |
| Quantity | int | Number of items sold |
| Discount | float | Discount applied (0.0 – 0.8) |
| Profit | float | Profit earned (can be negative) |

**Key statistics:**
- **Total Sales:** $2,296,195.59
- **Total Profit:** $286,241.42
- **Average Sales per Order:** $230.15
- **Average Profit per Order:** $28.69
- **Duplicates found & removed:** 17

---

##  Analysis Performed

### 1. Data Cleaning & Preparation
- Loaded and inspected the dataset with `df.info()` and `df.describe()`
- Identified and removed **17 duplicate records**
- Verified zero null values across all columns

### 2. Regional Performance
- **Sales by Region** — West ($725K) leads, followed by East ($678K), Central ($501K), and South ($392K)
- **Profit by Region** — West ($108K) is the most profitable; Central ($40K) lags despite moderate sales

### 3. Category & Sub-Category Analysis
- **Sales by Category** — Technology ($836K) > Furniture ($741K) > Office Supplies ($719K)
- **Profit by Category** — Technology ($145K) and Office Supplies ($122K) outperform Furniture ($18K)
- **Sub-Category Profit** — Copiers, Phones, and Accessories are the most profitable; **Tables (−$17.7K)** and **Bookcases (−$3.5K)** generate losses

### 4. Discount vs Profit Analysis
- Scatter plot reveals a clear **inverse relationship** — higher discounts correlate with lower (often negative) profits
- Excessive discounting erodes margins significantly

### 5. Top Cities by Sales
- **New York City** ($256K), **Los Angeles** ($176K), and **Seattle** ($119K) are the top-performing cities

### 6. Furniture Deep-Dive
- Within Furniture: Chairs ($26.6K profit) and Furnishings ($13K) are profitable
- **Tables** and **Bookcases** consistently generate losses — requires pricing/supply chain review

---

## 📊 Visualizations

The notebook produces the following charts (screenshots saved in `images/`):

### Total Sales by Region
> West leads with $725K in total sales, followed by East, Central, and South.

![Total Sales by Region](images/Screenshot_17-7-2026_16327_localhost.jpeg)

### Total Profit by Region
> West is also the most profitable ($108K), while Central lags at $40K despite moderate sales.

![Total Profit by Region](images/Screenshot_17-7-2026_163227_localhost.jpeg)

### Sales by Category
> Technology ($836K) edges out Furniture ($741K) and Office Supplies ($719K).

![Sales by Category](images/Screenshot_17-7-2026_163256_localhost.jpeg)

### Profit by Category
> Technology and Office Supplies dominate profits; Furniture contributes only $18K.

![Profit by Category](images/Screenshot_17-7-2026_163410_localhost.jpeg)

### Profit by Sub-Category
> Copiers, Phones, and Accessories are the top earners. Tables and Bookcases generate losses.

![Profit by Sub-Category](images/Screenshot_17-7-2026_163430_localhost.jpeg)

### Discount vs Profit
> Higher discounts correlate strongly with lower (often negative) profits.

![Discount vs Profit](images/Screenshot_17-7-2026_163455_localhost.jpeg)

---

##  Key Findings

- The **West region** generated the highest overall sales and profit.
- **Technology** was the highest-performing category in terms of revenue.
- Certain furniture sub-categories (**Tables**, **Bookcases**) generated negative profits despite contributing to sales.
- **New York City** and **California** contributed significantly to overall sales.
- **Higher discounts** were generally associated with **lower profitability**.
- A relatively small group of customers contributed a disproportionately high share of total profit.

---

##  Business Recommendations

1. **Review the discount policy** to prevent excessive profit loss.
2. **Focus marketing efforts** on high-performing regions while identifying reasons behind weaker regional performance.
3. **Re-evaluate pricing and inventory** strategies for consistently loss-making products (Tables, Bookcases).
4. **Increase investment** in high-profit product categories (Technology, Office Supplies).
5. **Develop customer retention** strategies for high-value customers through loyalty programs and personalized offers.
6. **Monitor profitability continuously** instead of focusing solely on sales volume.

---

##  Future Scope

- Build an **interactive Power BI dashboard** for dynamic exploration
- Develop **predictive models** to forecast future sales
- Perform **customer segmentation** using clustering techniques
- Conduct **time-series analysis** if order dates become available
- Create **automated reporting pipelines** for business users

---

##  Tech Stack

| Tool | Purpose |
|---|---|
| **Python 3.14** | Programming language |
| **Pandas** | Data manipulation & analysis |
| **NumPy** | Numerical operations |
| **Matplotlib** | Data visualization |
| **Jupyter Notebook** | Interactive development environment |

---

##  Getting Started

### Prerequisites
- Python 3.x
- Jupyter Notebook or JupyterLab

### Installation

```bash
# Clone the repository
git clone https://github.com/<SudeeptoEENGNR>/Retail-Sales-Analysis.git
cd Retail-Sales-Analysis

# Install dependencies
pip install pandas numpy matplotlib jupyter

# Launch the notebook
jupyter notebook Sales_analysis.ipynb
```

---

##  License

This project is open-source and available for educational and personal use.

---

##  Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.
