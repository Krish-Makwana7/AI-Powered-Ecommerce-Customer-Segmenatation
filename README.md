# AI-Powered-Ecommerce-Customer-Segmenatation

> **AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026 | BharatCares**

---

## Project Overview

This project presents a complete, end-to-end data analytics solution built on the **Brazilian E-Commerce Public Dataset by Olist**. Using Python and AI-assisted analytics (Google Gemini), it transforms raw e-commerce transaction data into actionable business intelligence — covering sales trends, product performance, customer segmentation, geographic analysis, and statistical hypothesis testing.

---

## Problem Statement

E-commerce businesses generate large volumes of transaction data that, without systematic analysis, remain underutilized. This project addresses the challenge of extracting meaningful business insights from multi-table e-commerce data by:

- Identifying sales trends and seasonality
- Understanding customer purchasing behavior
- Segmenting customers by value and frequency
- Identifying high-performing product categories and geographic markets

---

## Objectives

1. Analyze delivered sales value trends over time (monthly and yearly)
2. Identify top-performing product categories by delivered sales value
3. Distinguish one-time vs. repeat customers and compare their value
4. Segment customers into four behavioral segments
5. Map delivered sales value across 27 Brazilian states
6. Identify product categories preferred by high-value repeat customers
7. Perform statistical hypothesis testing on customer value differences
8. Generate actionable business insights and recommendations
9. Document AI integration throughout the analytical workflow

---

## Dataset

**Name:** Brazilian E-Commerce Public Dataset by Olist  
**Source:** Kaggle — https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce  
**License:** CC BY-NC-SA 4.0

### Required CSV Files

| File | Description |
|------|-------------|
| `olist_orders_dataset.csv` | Order-level records with status and timestamps |
| `olist_order_items_dataset.csv` | Line items: product, price, freight value |
| `olist_customers_dataset.csv` | Customer unique IDs, city, state |
| `olist_products_dataset.csv` | Product metadata and category names |
| `product_category_name_translation.csv` | Category name translation (PT → EN) |

See [`data/README.md`](data/README.md) for download and setup instructions.

---

## Technologies Used

| Tool / Library | Purpose |
|----------------|---------|
| Python 3.8+ | Core programming language |
| Google Colab | Primary development environment |
| Pandas | Data loading, cleaning, merging, aggregation |
| NumPy | Numerical operations |
| Matplotlib | All data visualizations |
| SciPy | Statistical hypothesis testing (Welch's t-test) |
| Google Gemini | AI-assisted analytics, code generation, interpretation |
| python-docx | DOCX report generation |

---

## Project Workflow

```
Raw CSV Files
     ↓
Data Loading (with error handling)
     ↓
Data Inspection & Quality Assessment
     ↓
Data Cleaning (missing values, types, categories)
     ↓
Data Integration (multi-table merge)
     ↓
Feature Engineering (sales_value, customer segments)
     ↓
Delivered Order Filter
     ↓
Exploratory Data Analysis
     ↓
5 Business Questions Answered
     ↓
Customer Segmentation (4 segments)
     ↓
Statistical Hypothesis Testing (H1, H2, H3)
     ↓
Key Observations → Business Insights → Recommendations
     ↓
AI Integration Documentation
     ↓
Final Conclusion & Project Summary
```

---

## Key Findings

1. **November 2017** recorded the highest monthly delivered sales value at **BRL 1,153,364.20**
2. **Health & Beauty** was the highest-selling product category with delivered sales value of **BRL 1,412,089.53**
3. **Repeat customers** had a higher average delivered sales value per customer than one-time customers: **BRL 308.53 vs BRL 160.73**
4. **São Paulo (SP)** recorded the highest delivered sales value among Brazilian states: **BRL 5,769,703.15**
5. **High-value customers** contributed substantially more delivered sales value than low-value customers: **BRL 12,463,585.98 vs BRL 2,956,187.77**

> Note: All values above are computed dynamically by the notebook. Actual results depend on the dataset version used.

---

## Business Insights

1. November 2017 showed the strongest monthly delivered sales value, indicating a period of particularly high purchasing activity
2. Health & Beauty generated the highest delivered sales value among product categories, making it a key area for business analysis
3. Repeat customers showed a higher average delivered sales value per customer than one-time customers, demonstrating an association between repeat purchasing and higher customer value
4. São Paulo recorded the highest delivered sales value among all states, indicating strong sales activity in this geographic market
5. High-value customers contributed substantially more delivered sales value than low-value customers, highlighting the importance of understanding higher-value customer segments

---

## Recommendations

1. **Strengthen customer retention** using personalized offers, relevant product recommendations, and targeted follow-up campaigns for repeat and high-value customers
2. **Prioritize high-performing categories** such as Health & Beauty, Watches & Gifts, and Bed Bath & Table to identify demand, pricing, and product-level opportunities
3. **Develop region-specific strategies** by analyzing customer preferences and demand patterns across Brazilian states, with particular attention to high-sales markets such as São Paulo

---

## How to Run

### Google Colab (Recommended)

1. Download the Olist dataset from Kaggle:  
   https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

2. Extract the ZIP archive to get the CSV files

3. Upload CSV files to **Google Drive** or directly to a **Colab session**

4. Open the notebook in Google Colab:
   - Upload `YOURNAME_AI_Powered_Ecommerce_Customer_Segmentation.ipynb`
   - Or open from GitHub via: `File → Open notebook → GitHub`

5. Update `DATA_PATH` in **Section 6** to match your file location:
   ```python
   # If files are in Google Drive:
   DATA_PATH = "/content/drive/MyDrive/olist_data/"
   
   # If files are uploaded directly to Colab:
   DATA_PATH = "/content/olist_data/"
   ```

6. Run all cells from top to bottom:
   - `Runtime → Run all` or press `Ctrl+F9`

7. Review generated tables and visualizations in each section

### Local Jupyter

```bash
git clone https://github.com/YOUR_USERNAME/ai-powered-ecommerce-customer-segmentation.git
cd ai-powered-ecommerce-customer-segmentation
pip install -r requirements.txt

# Place CSV files in the data/ directory
# Update DATA_PATH = "data/" in the notebook

jupyter notebook YOURNAME_AI_Powered_Ecommerce_Customer_Segmentation.ipynb
```

### Generate DOCX Report

```bash
pip install python-docx
python generate_report.py
# Output: YOURNAME_ProjectReport.docx
```

---

## Project Files

| File | Description |
|------|-------------|
| `YOURNAME_AI_Powered_Ecommerce_Customer_Segmentation.ipynb` | Main Jupyter Notebook (26 sections) |
| `requirements.txt` | Python package dependencies |
| `YOURNAME_ProjectReport.docx` | Full academic project report |
| `generate_report.py` | Script to generate the DOCX report |
| `README.md` | This file |
| `data/README.md` | Dataset download and setup instructions |
| `outputs/figures/` | Generated chart images |
| `outputs/tables/` | Exported analysis tables |
| `.gitignore` | Excludes dataset CSVs and cache files |

---

## AI Integration

**AI Tool Used:** Google Gemini  
**Platform:** Google Colab

Google Gemini was used as an analytical assistant throughout this project for:

- Generating and explaining Python code for data loading, cleaning, and analysis
- Suggesting appropriate analytical approaches and visualization types
- Supporting exploratory data analysis and pattern identification
- Helping interpret statistical results and convert them into business language
- Developing hypotheses and business recommendations
- Debugging and improving analytical code

**Important:** AI assistance was used to augment the analytical process. All numerical results were computed by Python from the actual dataset and validated independently.

**AI Workflow:**
```
Business Question
      ↓
Prompt Google Gemini
      ↓
Generate / Explain Code
      ↓
Run in Google Colab
      ↓
Inspect Results
      ↓
Validate Calculations
      ↓
Interpret Findings
      ↓
Generate Business Insight
```

---

## Validation

All numerical findings in this project are computed dynamically from the dataset using Python. Expected values documented in the notebook serve as **validation targets** — the notebook calculates actual values and prints them for verification. No values are hard-coded.

---

## Limitations

- The dataset represents **historical** e-commerce activity; findings may not reflect current market conditions
- **Early (2016) and late (2018) periods** may contain incomplete observations due to partial data coverage
- **State-level sales differences** are descriptive and may reflect customer population, market size, or order volume rather than causal factors
- This is **observational data** — no causal relationships can be established from the analysis
- **Customer segmentation** results depend on the selected methodology (median-based threshold); different thresholds produce different segments
- The dataset does not include product pricing changes over time or promotional information

---

## Conclusion

This project demonstrates a complete data analytics workflow — from raw multi-table e-commerce data through cleaning, integration, EDA, segmentation, hypothesis testing, and business insight generation. The analysis identified key patterns in sales trends, product performance, customer behavior, and geographic distribution. AI assistance (Google Gemini) accelerated the analytical process while all results were validated computationally. The project is structured to be reproducible, academically rigorous, and suitable for professional presentation.

---

## References

- Olist Brazilian E-Commerce Dataset: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
- Pandas Documentation: https://pandas.pydata.org/docs/
- Matplotlib Documentation: https://matplotlib.org/stable/
- SciPy Documentation: https://docs.scipy.org/doc/scipy/
- Google Gemini: https://gemini.google.com/

---

*AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026 | BharatCares*
