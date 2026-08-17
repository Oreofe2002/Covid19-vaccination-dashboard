# Global COVID-19 Visual Audit & Vaccination Tracker 🌍

An interactive, responsive dual-page business intelligence application built using Python (Pandas) for data engineering and Tableau Public for analytical dashboard architecture.

## 📊 Live Interactive Dashboards
👉 [Click here to view the Interactive Tableau Dashboard](PASTE_YOUR_TABLEAU_PUBLIC_SHARE_LINK_HERE)

---

## 🛠️ Data Pipeline & Engineering Architecture
The underlying dataset was processed through a robust data engineering pipeline written in Python to ensure data integrity and dashboard query optimization:
* **Data Cleaning & Filtering**: Dropped non-country aggregation rows and eliminated unnecessary metrics to optimize performance.
* **Missing Value Imputation**: Implemented a forward-fill (`ffill()`) time-series function grouped by country to bridge historical recording gaps.
* **Feature Engineering**: Pre-calculated foundational rate fields (e.g., `vaccination_coverage` and `fatality_rate`) using advanced row-by-row matrix math.
* **Level of Detail Stabilization**: Engineered advanced LOD metrics inside Tableau (`{FIXED [Location] : MAX([Total Cases])}`) to handle multi-year timeseries date anomalies and bypass outlier data glitches.

---

## 💡 Key Analytical Insights
### 1. Executive Summary (Dashboard Page 1)
* **Macro Matrix Row**: A fully responsive row of 5 high-impact KPIs detailing global reach metrics across 243 countries.
* **Geographic Choropleth Map**: Tracks relative vaccine dispersion across the globe.
* **Timeline Velocity Wave**: Maps out the absolute speed and wave momentum of the pandemic using continuous monthly date baselines.

### 2. Deep-Dive Analytics (Dashboard Page 2)
* **Vaccine Hesitancy & Vulnerability Matrix**: Isolates critical public health hotspots with high case counts but dangerously low coverage rates (under 30%).
* **Inoculation vs. Mortality Scatter Plot Grid**: Generates a clear visualization proving the negative correlation between protection levels and case fatality trends.

---

## 🗂️ Repository File Structure
* `covid_data_cleaning.ipynb`: The complete Python cleaning scripts, error adjustments, and calculation pipelines.
* `covid_dashboard_clean.csv`: The verified, production-ready dataset utilized as the direct Tableau database source asset.
