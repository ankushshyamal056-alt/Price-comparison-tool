# 🛒 HP Pavilion Price Comparison Tool

A data analytics project that scrapes HP Pavilion laptop listings from **Amazon India** and **Flipkart**, performs exploratory data analysis (EDA), and generates visual insights to support data-driven buying decisions.

---

## 📌 Project Overview

This project automates the collection of product data across two major Indian e-commerce platforms and applies statistical and visual analysis to answer key questions:

- Which platform offers better prices?
- Is there a relationship between price and customer ratings?
- How are HP Pavilion laptops distributed across price segments?
- Which products offer the best value for money?

---

## 🔧 Tech Stack

| Category | Libraries |
|---|---|
| Web Scraping | `Selenium`, `WebDriver Manager` |
| Data Manipulation | `Pandas`, `NumPy` |
| Statistical Analysis | `SciPy` |
| Visualization | `Matplotlib`, `Seaborn` |

---

## 📂 Project Structure

```
Price_Comparison_Tool/
│
├── Price_Comparison_Tool.ipynb     # Main notebook
├── hp_pavilion_price_comparison.csv  # Scraped & merged dataset
└── hp_pavilion_analysis.png        # Output visualization dashboard
```

---

## 🚀 How It Works

### 1. Web Scraping
- Launches a Chrome browser using Selenium with a custom user-agent to avoid bot detection
- Scrapes up to **50 product listings** each from Amazon India and Flipkart
- Extracts: **Product Name**, **Price**, and **Customer Rating** per listing

### 2. Data Cleaning
- Strips currency symbols (`₹`) and commas from price strings
- Converts prices to numeric format and drops unparseable rows
- Filters results to keep only genuine HP products

### 3. Exploratory Data Analysis
- Descriptive statistics for price and rating across both platforms
- **95% Confidence Intervals** for mean prices (Amazon vs. Flipkart)
- **Independent T-Test** to determine if price differences are statistically significant
- **Pearson Correlation** between price and customer rating
- **Standard Deviation** comparison for pricing consistency

### 4. Price Segmentation
Products are categorized into four tiers:
- 🟢 **Budget** — Under ₹50,000
- 🟡 **Mid-range** — ₹50,000–₹65,000
- 🟠 **Premium** — ₹65,000–₹80,000
- 🔴 **High-end** — Above ₹80,000

### 5. Top Products Analysis
Identifies the:
- 5 most expensive products
- 5 best-rated products
- 5 best value-for-money products (via a custom `Value Score = rating / price × 10,000`)

### 6. Visualizations
A 2×3 subplot dashboard (`hp_pavilion_analysis.png`) covering:
- Price distribution histogram (by platform)
- Rating distribution histogram (by platform)
- Box plot of prices (by platform)
- Scatter plot of Price vs. Rating (with trendline)
- Average price bar chart (by platform)
- Average rating bar chart (by platform)

---

## 📊 Key Findings

- **Platform Pricing**: Both platforms are highly competitive, with overlapping confidence intervals indicating similar average pricing.
- **Price vs. Rating**: A **weak positive correlation** exists — higher-priced laptops tend to receive slightly better ratings, but price alone does not determine satisfaction.
- **Market Dominance**: Mid-range laptops dominate the listings, reflecting strong demand for value-for-money products.
- **Customer Sensitivity**: Visible discounts and promotional pricing significantly influence purchasing decisions.

---

## ⚙️ Setup & Usage

### Prerequisites
- Python 3.8+
- Google Chrome browser installed

### Installation

```bash
git clone https://github.com/your-username/Price_Comparison_Tool.git
cd Price_Comparison_Tool
pip install selenium webdriver-manager pandas numpy scipy matplotlib seaborn
```

### Run

Open and run `Price_Comparison_Tool.ipynb` in Jupyter Notebook or JupyterLab.

```bash
jupyter notebook Price_Comparison_Tool.ipynb
```

> **Note:** The scraping cells will open a Chrome browser window automatically. Ensure you have a stable internet connection. Website HTML structures may change over time, requiring XPath selector updates.

---

## 📈 Sample Output

The notebook generates `hp_pavilion_analysis.png` — a comprehensive dashboard with price and rating breakdowns by platform.

---

## 🧠 Skills Demonstrated

- Web scraping with browser automation
- Data cleaning and preprocessing
- Statistical hypothesis testing
- Exploratory data analysis (EDA)
- Business insight generation from raw data
- Data visualization

---

## 📬 Contact

Feel free to connect or reach out if you have questions or suggestions!

> ⭐ If you found this project useful, consider giving it a star!
