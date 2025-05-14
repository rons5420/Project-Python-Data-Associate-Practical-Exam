# Spectrum Shades LLC - Data Cleaning and Analysis

## Overview

This project addresses product quality issues at **Spectrum Shades LLC**, a supplier of concrete color solutions. The company has received customer complaints regarding **inconsistent color quality**, prompting the need for a data-driven investigation into potential causes and improvements.

The goal of this project is to clean and analyze the `production_data.csv` dataset, identify patterns behind color quality issues, and provide actionable insights that help reduce customer dissatisfaction and returns.

---

## Tasks Completed

### ✅ Task 1: Data Cleaning and Preparation
- **Handled missing values**, including unconventional formats like `'missing'`, `'-'`, and empty strings.
- **Standardized categorical values** by correcting typos, casing, and unexpected strings.
- Converted columns to appropriate **data types**.
- Replaced:
  - Missing `raw_material_supplier` with `'national_supplier'`
  - Missing `pigment_type` with `'other'`
  - Invalid or missing `pigment_quantity` with **median**
  - Missing `mixing_time` with **mean** (rounded to 2 decimals)
  - Missing `mixing_speed` with `'Not Specified'`
  - Missing `product_quality_score` with **mean** (rounded to 2 decimals)

### ✅ Task 2: Grouped Aggregation
- Calculated average `product_quality_score` and `pigment_quantity` grouped by `raw_material_supplier`.

### ✅ Task 3: Conditional Filtering
- Filtered data for batches using `international_supplier` with `pigment_quantity > 35 kg`.
- Computed the average `product_quality_score` for these filtered records.

### ✅ Task 4: Summary Statistics and Correlation
- Calculated:
  - **Mean and standard deviation** of `pigment_quantity` and `product_quality_score`
  - **Pearson correlation coefficient** between the two variables to assess linear relationship

---

## Output

- All final cleaned and intermediate DataFrames are named as required:
  - `clean_data`
  - `aggregated_data`
  - `pigment_data`
  - `product_quality`

---

## Tools Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib (if visualizations are added)**
- **Jupyter Notebook or Google Colab**

---

## Conclusion

Through this project, we identified data inconsistencies, handled them using systematic data cleaning steps, and uncovered how **supplier type** and **pigment quantity** influence **product quality**. The insights can directly help Spectrum Shades LLC improve their production process and customer satisfaction.

