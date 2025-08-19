# AICTE Skills4Future P-5: US Supply Chain Emission Factors Analysis

This repository contains data analysis, visualization, and machine learning modeling for US industry and commodity supply chain emission factors, as part of the AICTE Skills4Future program (Project 5). The goal is to analyze greenhouse gas (GHG) emission factors across industries and commodities (2010–2016), visualize insights, and build predictive models for emission factor estimation.

---

## 📁 Repository Structure

```
.
├── week-1.ipynb                             # Data Exploration & Visualization (Week 1)
├── Week2/
│   ├── week2task.ipynb                      # Data Processing & ML Model (Week 2)
│   ├── models/
│   │   ├── final_model.pkl                  # Trained RandomForestRegressor model
│   │   └── scaler.pkl                       # Fitted StandardScaler for features
│   └── SupplyChainEmissionFactorsforUSIndustriesCommodities.xlsx  # Main data source (2010–2016)
```

---

## 📊 Project Overview

- **Data Source:** US Supply Chain Emission Factors (2010–2016) across industries and commodities, including substance-level (CO₂, methane, N₂O, other GHGs) emission factors, data quality scores, and units standardized per 2018 USD.
- **Tasks Covered:**
  - Data cleaning and exploratory data analysis (EDA)
  - Visualization of emission factors by industry, substance, and year
  - Feature engineering and merging of multiple years' sheets
  - Building and saving a predictive model for emission factor estimation

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/preeti47g/AICTE-skills4future-P-5.git
cd AICTE-skills4future-P-5
```

### 2. Environment Setup

- Python >= 3.8 recommended
- Install requirements (main packages: pandas, numpy, scikit-learn, seaborn, matplotlib, joblib, openpyxl):

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib openpyxl
```

### 3. Data Files

- **SupplyChainEmissionFactorsforUSIndustriesCommodities.xlsx** in `Week2/` contains all years (2010–2016) as separate sheets for both commodities and industries.
- Outputs and models (`final_model.pkl`, `scaler.pkl`) are provided in `Week2/models/`.

---

## 📗 Notebooks

### [`week-1.ipynb`](./week-1.ipynb)
- **Purpose:** Data loading, cleaning, EDA, and visualization for a single summary CSV.
- **Key Steps:**
  - Importing libraries, loading CSV data
  - Data cleaning: handling missing values, type conversions
  - Descriptive statistics, data checks
  - Visualizations:
    - Top 10 industries by total emissions (bar, pie)
    - Emissions distribution histogram
    - Emissions by substance
    - Correlation heatmap for quality scores

### [`Week2/week2task.ipynb`](./Week2/week2task.ipynb)
- **Purpose:** Multi-year data ingestion, merged processing, feature engineering, and machine learning.
- **Key Steps:**
  - Loads all sheets for each year (2010–2016) for both commodities and industries
  - Cleans and merges, adds source/year columns
  - Drops irrelevant columns, summarizes data
  - Prepares data for ML: label encoding, scaling
  - Trains a RandomForestRegressor to predict emission factors
  - Saves the model (`final_model.pkl`) and scaler (`scaler.pkl`) for later inference

---

## 🤖 Model Artifacts

- **`Week2/models/final_model.pkl`**: Trained RandomForestRegressor for emission factor prediction.
- **`Week2/models/scaler.pkl`**: StandardScaler fitted to features, for consistent preprocessing during inference.

---

## 🗂️ Data Fields

- **Industry/Commodity Code, Name**
- **Substance**: `carbon dioxide`, `methane`, `nitrous oxide`, `other GHGs`
- **Emission Factors**: with/without margins (kg/2018 USD, purchaser price)
- **Data Quality (DQ)**: multiple reliability/correlation/collection scores
- **Year**: 2010–2016
- **Source**: `Industry` or `Commodity`

---

## 📈 Example Visualizations

- Bar plots of top-emitting industries/sectors
- Pie chart of emissions share by sector
- Histogram of emission factors
- Correlation heatmap for data quality

---

## 📝 How to Use

1. **Explore the Notebooks**  
   - Run `week-1.ipynb` for exploratory analysis and visualization on the summary CSV.
   - Run `Week2/week2task.ipynb` for full multi-year analytics and ML modeling.

2. **Model Inference**  
   - Use `final_model.pkl` and `scaler.pkl` to predict emission factors for new (compatible) input data.

---

## 🧑‍💻 Contributors

- [preeti47g](https://github.com/preeti47g)

---

## 📜 License

This repository is for educational purposes as part of the AICTE Skills4Future program. Attribution required for public or commercial use; see dataset origin for more information.

---

## 📬 Feedback

For questions or suggestions, please open an issue in this repository.
