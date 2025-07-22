
# CoreTrend Analyzer

CoreTrend Analyzer is a data science project aimed at analyzing chip specifications and market trends to drive business insights and product strategy.

## 🔍 Project Workflow

1. **Data Ingestion & Cleaning**
   - Load and preprocess raw chip specification data from `data/`.
   - Handle missing values, outliers, and anomalies (e.g., 0nm nodes, placeholder dates).

2. **Exploratory Data Analysis (EDA)**
   - Analyze chip specs, vendors, foundries, and performance features.
   - Identify trends in TDP, frequency, die size, GFLOPS, and release timing.

3. **Model Development**
   - Train CatBoost-based regression or classification models.
   - Store experimental models in `saved_models/` and final tuned models in `saved_models_final/`.

4. **Notebook for Analysis**
   - All processing and experimentation is documented in `notebook.ipynb`.

## 📊 Key Insights

### 1. Market Concentration
- AMD (34%), Intel (29%), NVIDIA (25%) dominate.
- Action: Leverage AMD scale, market NVIDIA as high-performance, emphasize Intel’s FP precision for HPC.

### 2. Foundry Strategy
- TSMC produces 45% of chips, followed by Intel (29%).
- Action: Deepen TSMC collaboration, improve smaller foundry tracking.

### 3. Product Launch Trends
- Peaks in 2013, seasonality in Q2 and January.
- Action: Align product launches with market cycles.

### 4. Node Size Analysis
- Common nodes: 14nm, 28nm. Median: 40nm.
- Action: Prioritize cost-effective nodes and remove erroneous data (0nm, 250nm).

### 5. TDP vs. Compute Efficiency
- GPUs have higher TDP and die size; NVIDIA leads high-performance segment.
- Action: Target low-TDP CPUs for mobile, market GPUs for AI workloads.

### 6. Compute Capability Clusters
- Mainstream GPUs: 240–384 FP32 GFLOPS.
- Action: Create tiered SKUs (mainstream, value, flagship).

### 7. Data Gaps
- High missing rates in GFLOPS specs.
- Action: Strengthen data sourcing to boost analytics and marketing.

### 8. Feature Correlation
- FP32 ~ FP64 GFLOPS; Die Size ~ Transistor Count.
- Action: Simplify spec sheets for clarity.

### 9. Outlier Products
- AMD MI100 and NVIDIA A100 variants set benchmarks.
- Action: Use them in strategic marketing and as reference designs.

## 📁 Folder Structure

```
CoreTrend Analyzer/
├── .ipynb_checkpoints/
├── catboost_info/
├── data/                    # Raw and cleaned datasets
├── saved_models/            # Intermediate models
├── saved_models_final/      # Final tuned models
└── notebook.ipynb           # Main analysis and modeling notebook
```

## ✅ Next Steps

- Continue enriching the dataset with missing performance values.
- Explore interactive dashboards for technical and marketing teams.
- Evaluate chip clustering for portfolio optimization.

---

Developed with CatBoost and Python.
