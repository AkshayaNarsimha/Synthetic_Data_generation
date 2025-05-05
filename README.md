
# Synthetic Dataset Generation and Similarity Evaluation

This repository contains the implementation for the **coding task** in the GenAI PhD application (April 2025, BTH). The task involves generating a new synthetic dataset based on the characteristics of a provided dataset and verifying their statistical similarity.

## 📌 Objective

To generate a new dataset that is **structurally and statistically similar** to a given reference dataset—without copying its sampling parameters—and to **evaluate the similarity** using statistical tests and visual analysis.

## 📂 Files

├── synthetic_data_final.ipynb # Main Jupyter notebook with full code and analysis
├── original_dataset.csv # Original dataset provided
├── synthetic_dataset.csv # Generated synthetic dataset
├── EXPLANATION.md # Reasoning, limitations, and discussion

## 🧠 Methodology

1. **Data Generation**  
   The original dataset consists of:
   - A categorical column: `Category1` (values A-E)
   - Two continuous variables: `Value1` ~ N(10, 2), `Value2` ~ N(20, 6)

   The new synthetic data is generated using **different parameters** while preserving the **structure and distribution**:
   - Different sample size (1500)
   - Adjusted mean and std values for `Value1`, `Value2`
   - Custom category probabilities

2. **Statistical Evaluation**
   - ✅ **Kolmogorov-Smirnov (KS) test** for `Value1` and `Value2`  
   - ✅ **Chi-squared test of homogeneity** for `Category1`
   - ✅ Mean and standard deviation comparisons

3. **Visual Comparison**
   - Histograms
   - Box plots
   - Overlayed density plots

## ✅ Results Summary

- **KS Test**: Indicates high similarity in `Value2`, moderate for `Value1`
- **Chi-squared Test**: No significant difference in `Category1` at 95% confidence
- **Visuals**: Distribution shapes closely match between original and synthetic sets
- **Mean & Std Differences**: All values within an acceptable similarity margin

## 🔬 Insights & Reasoning

Please refer to [`EXPLANATION.md`](EXPLANATION.md) for:
- Design rationale
- Tuning strategies
- Interpretation of statistical results
- Acknowledged limitations and optional extensions

## 🛠️ Requirements

This code is written in Python 3. You can install dependencies using:
pip install -r requirements.txt

Required packages:
pandas
numpy
seaborn
matplotlib
scipy

▶️ How to Run
Clone this repo:
git clone https://github.com/AkshayaNarsimha/Synthetic_Data_generation.git

Open the notebook:
jupyter notebook synthetic_data_final.ipynb
Follow the step-by-step sections in the notebook to reproduce the dataset generation, visualizations, and evaluation.

🙋 Author
Akshaya Bathula
Ph.D. Applicant — GenAI, BTH
