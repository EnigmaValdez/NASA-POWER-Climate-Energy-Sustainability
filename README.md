# NASA-climate-energy-sustainability

Please see Google Doc here: https://docs.google.com/document/d/1kS_3-IHO0DqVIXuUWVn5cqDojmXkjyiAPDaAl13zSms/edit?tab=t.0

End-to-end data engineering and climate analysis project utilizing 16+ years of NASA POWER daily observations (2010–2026). Features a Power Query ETL pipeline, multi-year thermal and solar irradiance matrices, dynamic line PivotCharts, and strategic applications for Pasadena's aerospace and clean-energy sectors.

# NASA POWER Energy, Climatology & Sustainability Dataset Cleaning & Analysis

## Project Overview
This project involves the ingestion, cleansing, and transformation of a multi-year NASA POWER daily climatology and energy dataset (**6,147 rows**) spanning from 2010 to 2026[cite: 10.2]. The objective is to prepare clean, structured data for portfolio demonstration, targeting hiring managers in Pasadena's aerospace, clean-energy, and local tech ecosystems[cite: 10.2].

- Ingested and explored a raw, multi-year 6,000+ row NASA dataset[cite: 10.2].
- Cleaned and transformed it using Power Query (stripping messy metadata, promoting headers, enforcing strict data types, and neutralizing missing data flags)[cite: 10.2].
- Built validated monthly climate and solar irradiance Pivot Tables ready for executive review[cite: 10.2].

---

## Data Source
* **Dataset:** NASA POWER Native Resolution Daily Data (Latitude: 36.5328, Longitude: -119.2702)[cite: 10.2]
* **Parameters:** Surface solar irradiance (`ALLSKY_SFC_SW_DWN`), ambient surface temperature (`T2M`), dew/frost point, humidity, and wind characteristics[cite: 10.2].

---

## Data Cleaning & Transformation Pipeline (Power Query)
Following *Guerrilla Data Analysis* principles, the raw data dump was systematically transformed through the following steps[cite: 10.2]:
1. **Metadata Stripping:** Removed the top 28 rows containing descriptive header blocks, coordinate metadata, and parameter definitions[cite: 10.2].
2. **Header Promotion:** Promoted the true data header row (`YEAR`, `MO`, `DY`, parameters) to official column headers[cite: 10.2].
3. **Data Type Enforcement:** Verified and enforced strict data types (Whole Numbers for date components, Decimal Numbers for meteorological and energy metrics) to prevent calculation errors[cite: 10.2].
4. **Handling Missing Data Flags:** Replaced NASA's standard missing data flag (`-999`) across numeric measurement columns with `null` values to maintain statistical integrity and prevent skewed averages[cite: 10.2].
5. **Loading & Structuring:** Loaded the clean dataset into a dynamic, formatted Excel Table (`NASA_Climate_Data`) ready for aggregation, Pivot Tables, and visualization[cite: 10.2].

---

## Exploratory Data Analysis & Analytical Matrices

### 1. Multi-Year Thermal Matrix (`MultiYear Temp Matrix`)
* **Structured Year-over-Year Analysis:** Built a comprehensive multi-year temperature matrix (`YEAR` in columns, months 1–12 in rows, and `Average of T2M` in values) spanning a 16+ year timeline from 2010 to 2026[cite: 10.2].
* **Design & Layout Principles:** Formatted following Oz du Soleil's professional Tabular Layout standards with grand totals disabled to maintain a clean, executive-level presentation[cite: 10.2].
* **Exploratory Insights & Visualization:** Seamlessly pairs with a dynamic line PivotChart to immediately capture seasonal thermal curves—consistently highlighting peak summer temperatures exceeding 30°C and winter troughs near 10°C—providing essential baseline data for environmental and energy load modeling[cite: 10.2].

### 2. Multi-Year Clean Energy Analysis: Surface Solar Irradiance (`Solar_Irradiance_Matrix`)
* **Dedicated Analytical Tab:** Created a second structured Pivot Table mapping multi-year surface solar shortwave downward irradiance (`ALLSKY_SFC_SW_DWN`) across a 16+ year timeline (2010–2026)[cite: 10.2].
* **Layout & Standardization:** Configured using Oz du Soleil's Tabular Layout methodology with grand totals disabled, aligning seamlessly with the multi-year temperature matrix structure for executive review[cite: 10.2].
* **Clean-Energy & Photovoltaic Potential:** Captures monthly and yearly solar availability patterns, providing crucial metrics for environmental modeling, solar energy forecasting, and sustainable infrastructure planning in Southern California[cite: 10.2].

---

## Executive Summary & Local Industry Recommendations

### Project Summary
This project delivers an end-to-end data pipeline and exploratory analysis utilizing 16+ years of daily climate, energy, and sustainability observations (2010–2026) from the NASA POWER dataset for the Pasadena region (Latitude: 36.5328, Longitude: -119.2702)[cite: 10.2]. Utilizing Power Query for robust data ingestion, missing-value neutralization, and type enforcement, the raw data was transformed into a multi-tab analytical model in Excel[cite: 10.2]. The workbook features structured Pivot Table matrices and dynamic PivotCharts following Oz du Soleil's *Guerrilla Data Analysis* methodology, tracking long-term trends in monthly surface temperature (`T2M`) and surface solar shortwave downward irradiance (`ALLSKY_SFC_SW_DWN`)[cite: 10.2].

### Strategic Industry Recommendations for Pasadena Employers

* **Aerospace & Systems Engineering (JPL / Defense Sector):**
  * **Application:** Multi-year thermal matrix (`MultiYear Temp Matrix`) and dynamic line charts provide baseline historical temperature volatility exceeding 30°C in peak summer months[cite: 10.2].
  * **Recommendation:** Aerospace and thermal engineering teams can leverage this multi-year baseline data for environmental testing simulations, thermal dissipation modeling, and structural material behavior analysis under extreme regional weather variations[cite: 10.2].

* **Clean Energy & Sustainability (Local Solar / Grid Infrastructure):**
  * **Application:** The dedicated surface solar irradiance matrix (`Solar_Irradiance_Matrix`) quantifies shortwave downward solar energy availability across seasonal cycles from 2010 to 2026[cite: 10.2].
  * **Recommendation:** Renewable energy analysts and smart-grid operators can utilize these historical irradiance metrics to refine photovoltaic (PV) yield estimations, optimize solar array placement, and improve seasonal electrical grid load forecasting across Southern California[cite: 10.2].
