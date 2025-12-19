# 📊 Retail Market Intelligence: Big Data Analysis with Google BigQuery

> **Academic Capstone Project**: Comprehensive analysis of **1.39 million retail products** across **248 categories** using Google BigQuery, Python, and AI-powered analytics to deliver actionable business insights as an analytics consultant.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![BigQuery](https://img.shields.io/badge/Google-BigQuery-blue.svg)](https://cloud.google.com/bigquery)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

## 🎯 Project Overview

**Context**: Final assignment for Big Data Workflows in AI-Powered Business Analytics (Hult International Business School)

**Role**: Analytics and Decision Support Consultant

**Objective**: Extract compelling, non-trivial business insights from extensive retail product data to demonstrate potential value for a prospective retail client.

**Scope**: Analyze 1.39M+ products across 248 categories using Google BigQuery, delivering strategic insights backed by rigorous data analysis, documented SQL queries, and professional visualizations.

**Achievement**: Exceeded requirements by delivering **12 comprehensive analyses** (5 required), each with full documentation, reproducible queries, and strategic recommendations.

## 📋 Assignment Requirements Met

| Requirement | Delivered | Evidence |
|------------|-----------|----------|
| **5+ Non-Trivial Insights** | ✅ 12 comprehensive analyses | Category performance, market efficiency, bestseller patterns, pricing optimization |
| **Business Value** | ✅ Strategic recommendations | $84.2M market analyzed with actionable growth strategies |
| **Documented Queries** | ✅ Full SQL + Vanna.AI workflow | All queries documented with outputs and explanations |
| **Visualizations** | ✅ 15+ professional charts | Performance metrics, correlation analysis, distribution patterns |
| **Reproducibility** | ✅ Complete "paper trail" | Step-by-step methodology with code and results |
| **Original Analysis** | ✅ Custom queries beyond training notebook | 12 unique research questions with novel insights |

### Key Findings

- **Category efficiency matters more than execution**: 18x performance gap between efficient and inefficient categories
- **Accessibility beats exclusivity**: Bestsellers are priced 28% lower than regular products
- **Market selection > Perfect execution**: Being in the right category with average performance beats being excellent in a saturated market
- **Sweet spot pricing**: $10-25 price range optimizes both customer satisfaction and market penetration

## 🔍 Business Questions Answered

1. **Which categories offer the best growth opportunities?**
   - Health & Household leads with 547.7 volume per product (5.9x market average)
   - Tools & Home Improvement shows highest new product success rate (14.5%)

2. **What makes products successful?**
   - Universal appeal + affordability + frequency of use = Success
   - Bestsellers achieve 16x higher sales with 28% lower prices

3. **Where are the market inefficiencies?**
   - 84% of categories operate in low-efficiency zones
   - Toys & Games shows 81.3% performance gap despite largest catalog

4. **What pricing strategy works best?**
   - $10-25 "sweet spot" delivers optimal satisfaction (4.42 stars)
   - Premium pricing ($100+) suffers from expectation gaps (6.5% dissatisfaction)

## 🛠️ Technologies & Tools

### Data Infrastructure
- **Google BigQuery**: Large-scale data warehousing and SQL processing
- **Vanna.AI**: AI-powered SQL query generation and optimization

### Analysis & Visualization
- **Python 3.8+**
  - `pandas`: Data manipulation and analysis
  - `matplotlib` & `seaborn`: Statistical visualization
  - `plotly`: Interactive charts
- **Jupyter Notebook**: Interactive development environment
- **Looker Studio**: Dashboard creation

### AI/ML Tools
- **Claude (Anthropic)**: Analysis assistance and insight generation
- **ChatGPT**: Documentation and reporting

## 📈 Key Analyses Performed

### 1. **Category Performance Analysis**
- Analyzed 248 product categories across multiple dimensions
- Identified efficiency tiers and saturation levels
- Performance scoring using composite metrics

### 2. **Market Efficiency Modeling**
```sql
-- Efficiency tier classification
CASE
  WHEN avg_sales_per_product > 2000 THEN 'Super Efficient'
  WHEN avg_sales_per_product > 1000 THEN 'High Efficiency'
  WHEN avg_sales_per_product > 500 THEN 'Moderate Efficiency'
  ELSE 'Low Efficiency'
END as efficiency_tier
```

### 3. **Bestseller Pattern Recognition**
- Identified key characteristics of top performers
- Analyzed 8,430 bestsellers vs 1.25M regular products
- Discovered the "bestseller flywheel effect"

### 4. **Price-Value Optimization**
- Value score calculation: `stars / price` ratio
- Identified optimal pricing bands by category
- Expectation gap analysis for premium products

## 📊 Dataset Information

**Source**: Google BigQuery - `hultaibigdata.retail_products.products`

**Dataset Size**:
- Total Products: 1,393,564
- Categories: 248
- Price Range: $0.01 - $19,731.81
- Average Rating: 4.005 stars
- Time Period: Current snapshot with monthly sales data

**Key Fields**:
- `product_id`, `title`, `category_name`
- `stars`, `reviews`, `price`
- `boughtInLastMonth`, `isBestSeller`

## 🚀 Getting Started

### Prerequisites
```bash
# Python 3.8 or higher
python --version

# Google Cloud SDK (for BigQuery access)
gcloud --version
```

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/YashviNagda20/retail-market-intelligence-bigquery.git
cd retail-market-intelligence-bigquery
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Set up Google Cloud credentials**
```bash
# Authenticate with Google Cloud
gcloud auth login

# Set your project
gcloud config set project YOUR_PROJECT_ID
```

4. **Open Jupyter Notebook**
```bash
jupyter notebook notebooks/A1_BigData_Retail_Visuals.ipynb
```

## 📂 Project Structure

```
retail-market-intelligence-bigquery/
│
├── notebooks/
│   └── A1_BigData_Retail_Visuals.ipynb    # Main analysis notebook
│
├── reports/
│   ├── A1_Retail_Analysis_BigData_YN.pdf   # Comprehensive 33-page report
│   └── A1_BigData_Retail_Visuals_Yn.pdf    # Visual analysis summary
│
├── visualizations/
│   ├── category_performance.png
│   ├── efficiency_analysis.png
│   └── bestseller_comparison.png
│
├── sql_queries/
│   ├── category_analysis.sql
│   ├── efficiency_metrics.sql
│   └── bestseller_patterns.sql
│
├── requirements.txt                        # Python dependencies
└── README.md                               # This file
```

## 💡 Key Insights & Recommendations

### Strategic Recommendations

#### 1. **Category Selection Priority**
- **First Priority**: Tools & Home Improvement (14.5% bestseller rate, high ROI)
- **Second Priority**: Sports & Outdoors (balanced opportunity)
- **Golden Opportunity**: Health & Household (super efficiency + low saturation)

#### 2. **Pricing Strategy**
- Target $10-25 range for mass market products
- Avoid premium positioning unless exceptional quality is guaranteed
- Leverage accessibility over exclusivity

#### 3. **Product Development**
- Focus on **universal needs** + **daily use** + **problem-solving**
- Examples: Health & Household, Personal Care Products
- Avoid: Oversaturated hobby categories (Toys & Games)

#### 4. **Market Entry Tactics**
- Launch with high-frequency repurchase items
- Build review momentum early (social proof)
- Price competitively to gain initial traction

### Categories to Avoid
- **Toys & Games**: 81.3% below market average despite 12,118 products
- **Video Games**: Low bestseller rates, highly competitive
- **Home Décor**: Saturated with minimal differentiation

## 📸 Sample Visualizations

### Category Performance Overview
![Category Performance](visualizations/category_performance_overview.png)
*Analysis of top 15 categories by total monthly sales and efficiency*

### Market Efficiency Distribution
![Efficiency Analysis](visualizations/market_efficiency_scatter.png)
*Price vs Performance analysis showing efficiency tiers*

### Bestseller Comparison
![Bestseller Analysis](visualizations/bestseller_vs_regular.png)
*Key differences between bestsellers and regular products*

## 📝 Methodology

### Data Processing Pipeline
1. **Data Extraction**: SQL queries via Google BigQuery
2. **Data Cleaning**: Filtering invalid entries (price > 0, stars > 0)
3. **Feature Engineering**: Performance scores, efficiency metrics, value ratios
4. **Statistical Analysis**: Correlation analysis, distribution analysis
5. **Visualization**: Multi-dimensional visual exploration
6. **Insight Generation**: Pattern recognition and strategic recommendations

### Key Metrics Developed
- **Performance Score**: `stars * LOG(reviews + 1)`
- **Efficiency Ratio**: `avg_sales_per_product / category_average`
- **Value Score**: `average_rating / average_price`
- **Saturation Level**: Based on product count thresholds

## 🎓 Skills Demonstrated

### Technical Proficiency
- **Big Data Processing**: Google BigQuery SQL optimization, 1.39M+ record analysis
- **Data Analysis**: Python (pandas, numpy), statistical analysis, correlation matrices
- **Data Visualization**: matplotlib, seaborn, plotly, Looker Studio
- **AI Integration**: Vanna.AI for query optimization, LLMs for insight generation

### Business Analytics
- **Market Analysis**: Category performance evaluation, efficiency modeling
- **Strategic Recommendations**: Data-driven growth strategies, market positioning
- **KPI Development**: Custom performance metrics, composite scoring systems
- **Competitive Intelligence**: Bestseller pattern recognition, market saturation analysis

### Professional Competencies  
- **Requirements Analysis**: Exceeded 5-insight requirement with 12 comprehensive analyses
- **Documentation**: Complete reproducibility with SQL queries, code, and explanations
- **Presentation**: 33-page professional report with executive summary and visualizations
- **Critical Thinking**: Challenge conventional wisdom with data-driven insights

## 🔗 Related Projects

- [H1B Job Data Analysis](link) - Processing 561K immigration applications
- [World Happiness Index Dashboard](link) - 171 countries, 2015-2023
- [ESP32 Industrial IoT Counter](link) - Real-time production monitoring

## 📧 Contact

**Yashvi Nagda**
- 📧 Email: yashvinagda20@gmail.com
- 💼 LinkedIn: [linkedin.com/in/yashvi-nagda](https://www.linkedin.com/in/yashvi-nagda)
- 🌐 Portfolio: [Your Portfolio Website]

## 📄 License

This project is available for educational and portfolio purposes. Please credit if you use any analysis or code from this repository.

---

## 🎓 Academic Context

**Course**: Big Data Workflows in AI-Powered Business Analytics  
**Institution**: Hult International Business School  
**Program**: MS Business Analytics & MS International Marketing  
**Professor**: Pavel Paramonov  
**Date**: January 2025  
**Assignment Type**: Individual Final Project  

**Professor Guidance**: Analysis and decision support consulting approach with emphasis on non-trivial insights, business value, and complete documentation for reproducibility.

---

**⭐ If you found this project interesting, please star the repository!**

*This project demonstrates professional-level analytics work completed as part of advanced business analytics coursework.*

*Last Updated: January 2025*
