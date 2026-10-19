# 🐟 Lake Victoria Fisheries Supply Chain & Market Analytics Pipeline

## 📌 Project Overview
This project delivers a modular **Python data pipeline** designed to clean, transform, and analyze irregular fisheries monitoring survey records collected by the **Kenya Marine and Fisheries Research Institute (KMFRI)**. 

Field enumeration across remote landing sites and urban markets faces significant manual data-entry challenges. This system standardizes volatile records across **7 Kenyan counties**, calculating species volume distributions, localized price-per-kilogram margins, and processing value-addition matrices to help stakeholders optimize regional fish supply chains.

---

## 📁 Repository Structure
```text
├── data/
│   ├── raw/          # Immutable raw KMFRI survey data (kmfri_market_data.csv)
│   └── processed/    # Cleaned, parsed data ready for analysis
├── notebooks/        # Jupyter Notebooks for Exploratory Data Analysis (EDA)
├── src/              # Modular production Python code (data_pipeline.py)
├── reports/          # Generated business summaries and insights
│   └── figures/      # Exported data visualizations (Seaborn/Matplotlib charts)
├── .gitignore        # Caches, configuration, and data exclusions
├── requirements.txt  # Explicit project environment dependencies
└── README.md         # Professional portfolio documentation
```

---

## 🛠️ Technical Stack & Methodology
* **Language:** Python 3.x
* **Core Libraries:** `pandas` (Data manipulation), `numpy` (Vectorized mathematics), `matplotlib` & `seaborn` (Statistical visualization)
* **Execution Strategy:**
  1. **Data Ingestion & Sanitization:** Type casting dates, purging structural formatting artifacts, and resolving truck tracking omissions.
  2. **Feature Engineering:** Calculating standardized unit costs and value-add indexes per fish form.
  3. **Statistical Aggregation:** Grouping metrics by market, county, and species to identify supply constraints.

---

## 📈 Strategic Insights (Sample Discoveries)
* **Pelagic Bulk Flow:** Small pelagics (*Rastrineobola* / Local Name: *Omena*) dominate wholesale market volume footprints, flowing in dry bulks primarily toward major centers like **Gikomba Market (Nairobi)** and **Kibuye Wholesale Market (Kisumu)**.
* **Processing Premium Elasticity:** Table fish like *Tilapiines* (*Ngege*) and *Lates niloticus* (*Mbuta*) fetch maximum unit value when sold Fresh/Wet in urban spaces but rely heavily on traditional processing (Fried/Smoked) in rural sub-locations due to cold-chain deficits.

---

## 🚀 How to Run the Pipeline

### 1. Clone the Workspace
```bash
git clone https://github.com
cd kmfri-fisheries-analysis
```

### 2. Prepare Environment & Run
```bash
pip install -r requirements.txt
python src/data_pipeline.py
```
