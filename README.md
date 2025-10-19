# 🏬 Supermarket Coverage & Household Distribution Analysis (Singapore)

## 🧾 Summary
This project builds a data pipeline to analyse supermarket coverage in relation to household distribution across Singapore.  
By integrating **geospatial, demographic**, it provides data-driven insights for identifying strategic supermarket outlet locations.

---

## 📊 Data Sources
All datasets are official from [data.gov.sg](https://data.gov.sg):

- 🏪 **Supermarkets (GEOJSON)** – Singapore Food Agency, 2024  
- 🗺️ **Planning Area Boundaries (GEOJSON)** – Urban Redevelopment Authority (URA), 2024  
- 👨‍👩‍👧‍👦 **Household Population (CSV)** – Department of Statistics, 2025 (Census Of Population 2020) 

---

## ⚙️ Tech Stack
- **Languages & Tools:** Python (3.11), Jupyter Notebook  
- **Libraries:** pandas, geopandas, shapely, requests, SQLAlchemy  
- **Database:** PostgreSQL (cloud-hosted)  

---

## 🔁 Pipeline Workflow
- 🟢 **Extract** – Retrieved datasets via APIs from data.gov.sg  
- 🔄 **Transform** – Parsed formats, standardized field names, performed spatial joins, cleaned and merged data  
- 💾 **Load** – Uploaded structured tables into PostgreSQL with defined relationships for analysis  

---

## 🧩 Data Modeling
Data was organized through a **relational schema** linking:  
**Supermarket outlets → Planning Areas → Household data → Brands & Household sizes**

**Key tables include:**  
`planning_area`, `supermarket`, `population`, `household_size`

---

## ⚠️ Challenges & Limitations
- ❌ **Data coverage gaps:** Household dataset covers fewer planning areas than supermarket data  
- ⏳ **Data recency:** Census figures may not fully represent current household distribution  

---

## 🚀 Future Improvements
- 🏘️ Incorporate updated demographic and urban planning datasets (e.g., HDB dwelling units, URA statistics)  
- 📈 Enable **time-series tracking** for supermarket growth and population movement  
- 🤖 Automate pipeline scheduling for periodic refresh and improved scalability  

---

## 🧠 Skills Demonstrated
- 🌐 Data sourcing from open APIs and GEOJSON  
- 🗺️ Geospatial data handling and spatial joins  
- 🏗️ Database design and relational schema modelling  
- 🔄 ETL workflow development  
- ✅ Data validation and quality assurance
