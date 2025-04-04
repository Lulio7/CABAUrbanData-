# 📊 Buenos Aires Construction Dashboard

This project analyzes the evolution of construction activity in the City of Buenos Aires using public data from the "Obras Iniciadas" dataset. The result is a fully interactive dashboard built in Power BI.

---

## 📂 Dataset

- Source: [Buenos Aires Open Data Portal](https://data.buenosaires.gob.ar/dataset/obras-iniciadas)
- Description: The dataset contains detailed records of initiated construction projects in the city, including:
  - Neighborhood (Comuna)
  - Purpose (e.g. Housing, Commercial, Industrial)
  - Start Date of the work
  - Area to be constructed (in m²)
  - Construction permit ID

---

## 🔧 Project Workflow

### 1. Data Cleaning (Python)
- Libraries: `pandas`, `numpy`
- Handled:
  - Missing values and standardization of date fields
  - Derivation of time variables: `Year`, `Month`, `Quarter`
  - Outlier detection in surface area (e.g., filtering projects > 40,000 m²)

### 2. Data Modeling (Power BI - Power Query)
- Star schema approach:
  - Fact table: Construction projects
  - Dimension tables: Purpose, Neighborhood, Surface Ranges
- Created calculated columns for:
  - Surface area categorization (10 bins: 0–40,000 m²)
  - Month names with Spanish locale and capitalized format

### 3. DAX Measures
- `TotalWorks`: COUNT of unique IDs
- `AverageArea`: AVERAGE of surface to be built
- `TopNeighborhood`: Neighborhood with the highest number of projects
- `%ShareByPurpose`: Participation of each project purpose over total works

### 4. Visualizations
- Interactive Maps: Distribution of works by neighborhood
- Time Series: Monthly and yearly construction trends
- Area Distribution: Bar chart showing construction scale
- Slicers: Year, Purpose, Neighborhood, Area bin

---

## 📌 Business Questions Answered

- How has construction activity evolved year-over-year?
- Which neighborhoods show the highest volume of new works?
- Are most projects small-scale or large developments?
- What are the predominant purposes of construction?
- When are most projects initiated throughout the year?

---

## 🧩 Tools Used

- Python (ETL preprocessing)
- Power BI
- Power Query (M)
- DAX for KPI creation
- Geo-Spatial Visualization in Power BI

---

## 📈 Preview

Add a screenshot of the dashboard or GIF here.

---

## 💬 Contact

If you'd like to collaborate, ask questions or download the `.pbix` file, feel free to connect on [LinkedIn](https://www.linkedin.com/in/tu-usuario).

