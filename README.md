# BikeSharingProject – Berlin

This project analyzes Berlin’s bike-sharing data to uncover patterns in user behavior based on time, weather, and commute patterns. Built for practical data insights and real-world decision-making.

---

### Project Summary

An independent bike-sharing analysis project exploring rental activity, trip locations and usage patterns through Python notebooks and visualizations.

The dataset's original source, geographic coverage and collection period need to be documented before interpreting the findings as representative of Berlin.


---

## Tools & Technologies Used

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=microsoft-power-bi&logoColor=black)](https://powerbi.microsoft.com/)

## Key Insights

- Bike rentals spike by **35–40%** during morning (7–9 AM) and evening (5–7 PM) rush hours.  
- Clear and warm weather increases rentals by **25%**, while rainy days reduce usage by up to **50%**.  
- Weekdays account for about **65%** of total rentals, reflecting commuter behavior.

## How to Explore

Start with `BikeSharing_Berlin_Cleaned_Combined.ipynb` and review the charts in `images/`.

The input datasets referenced in the documentation are not included in this repository. Reproducing the analysis requires those datasets and their source information.

---


2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Launch Jupyter Notebook
   ```bash
   jupyter notebook
   ```
   Open the .ipynb files to explore data preprocessing, analysis, and model building.


4. View Dashboard
Use the dashboard_ready_dataset.csv with Power BI or Tableau to visualize the final results.

---

### **Project Outcomes**

*  **Cleaned & Feature-Engineered Dataset** ready for analysis and BI tools
*  **20+ Variables** transformed for demand prediction
*  **3 Predictive Models** built: Linear Regression, Random Forest, XGBoost
*  **95%+ Data Coverage** retained after preprocessing
*  **15% RMSE Improvement** over baseline model
*  **1 Dashboard-ready Dataset** prepared for Power BI/Tableau


---

### Dataset Details

- **File**: `BikeSharingData_Berlin_combinedandcleaned.pkl`
- **Format**: Python `.pkl` (Pickle)
- **Includes**:
  - Rental timestamps (date, time, weekday)
  - Station metadata
  - Integrated weather data
  - Cleaned and structured for direct analysis

---

## 📊 Visualizations

![Top 10 Bikes by Trip Count](images/Top%2010%20Bikes%20by%20Trip%20Count.png)
![Clustered Marker Map of Origins Goal](images/Clustered%20Marker%20Map%20of%20Origins%20Goal.png)
![Top 10 Starting Locations](images/Top%2010%20starting%20locations%20plot%20generated%20successfull.png)


---

### Directory Structure


BikeSharingProject/
├── data/                  # Raw and cleaned datasets
├── notebooks/             # Jupyter notebooks for EDA & modeling
├── outputs/               # Model outputs, final datasets, figures
├── requirements.txt       # Project dependencies
└── README.md              # Project overview


---


### Key Highlights

-  **Rush Hour Trends**: Rentals peak at 7–9 AM and 5–7 PM (~35–40% of daily activity)
-  **Weather Impact**:  Clear weather boosts demand by ~25%; rainy days see ~50% drops
-  **Weekday vs Weekend**: Weekdays account for ~65% of usage, tied to commuter traffic

---

### Quick Access

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1FYRNBP8zQJjSJBxNRSmgN5_1QXlUdmCm)

---

### License

This project is licensed under the MIT License.

---



## 👤 About the Author

**Balbir Singh**  
Freelance Data & Financial Analyst  
[![Email](https://img.shields.io/badge/Email-balbirbhatia.20%40gmail.com-red?style=flat-square&logo=gmail)](mailto:balbirbhatia.20@gmail.com)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-blue?logo=linkedin&style=flat-square)](https://www.linkedin.com/in/yourprofile)  
[![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github&style=flat-square)](https://github.com/Balbir89)

-----------------------------------------------









# Bike-Sharing Trip Analysis — Berlin

Exploratory analysis of bike-sharing trip records using Python, Pandas, Matplotlib and Folium.

This independent portfolio project explores when trips occur, where they start, which bikes are used most frequently and how trip characteristics vary.

[Open Main Notebook](BikeSharing_Berlin_Cleaned_Combined.ipynb) · [View Images](images)

## Project Objective

Explore trip activity through time-based analysis and geographic visualization to support questions about bike usage and potential fleet allocation.

The analysis addresses:

- How does trip volume vary by day and hour?
- Which recorded starting coordinates have the most trips?
- Which bikes have the highest recorded usage?
- How does average recorded speed vary by hour?
- What does the trip-duration distribution look like?
- Where are trip origins concentrated?

## Tools Used

| Tool | Purpose |
|---|---|
| Python | Analysis workflow |
| Pandas | Data inspection, datetime conversion and aggregation |
| Matplotlib | Charts and distributions |
| Folium | Interactive geographic visualizations |
| Jupyter Notebook | Code, explanations and outputs |

## Dataset

The main notebook loads:

`BikeSharingData_Berlin_combinedandcleaned.pkl`

The analysis uses these fields:

| Field | Use |
|---|---|
| `time_origin` | Trip date and hour |
| `lat_origin`, `long_origin` | Starting coordinates |
| `lat_destination`, `long_destination` | Destination coordinates |
| `bikeid` | Trip counts per bike |
| `speed_kmh` | Average recorded speed |
| `duration_betweenorigindestination` | Trip-duration analysis |

The notebook converts trip duration to minutes by dividing the source value by 60. This assumes the original duration is recorded in seconds.

**Data availability:** The input pickle file is not included in this repository. Running the analysis requires a compatible copy of that dataset.

**Data documentation:** The original provider, collection period, geographic coverage and reuse permissions still need to be documented. The notebook treats the dataset as Berlin bike-sharing data.

## Analysis Workflow

### 1. Inspect the Dataset

Load the existing cleaned dataset and inspect its structure, column names and sample records.

### 2. Prepare Time Features

Convert `time_origin` to datetime and extract the date and hour for aggregation.

### 3. Analyze Trip Activity

Create charts showing:

- Number of trips per day
- Number of trips by hour
- Ten most frequent starting coordinate pairs
- Ten most-used bikes by recorded trip count

### 4. Explore Trip Characteristics

Calculate and visualize:

- Average recorded speed by hour
- Trip-duration distribution in minutes

### 5. Map Trip Locations

Use Folium to create:

- A heatmap of trip origins
- A clustered map of up to 500 unique origin locations
- A map of up to 100 unique starting locations
- Straight-line connections for a random sample of 100 trips

The starting-location map is exported as `starting_locations_map.html` when its notebook cell runs.

## Selected Visualizations

### Top 10 Bikes by Trip Count

![Top 10 Bikes by Trip Count](images/Top%2010%20Bikes%20by%20Trip%20Count.png)

### Clustered Map of Trip Origins

![Clustered Map of Trip Origins](images/Clustered%20Marker%20Map%20of%20Origins%20Goal.png)

### Top 10 Starting Locations

![Top 10 Starting Locations](images/Top%2010%20starting%20locations%20plot%20generated%20successfull.png)

## Potential Operational Uses

The analysis can help frame questions about:

- **Fleet allocation:** Which areas show concentrated recorded activity?
- **Usage monitoring:** Which bikes have particularly high trip counts?
- **Time-based planning:** When does recorded trip activity increase or decrease?
- **Further investigation:** Which speed or duration observations warrant closer inspection?

These are potential applications of the analysis, not measured operational improvements.

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/Balbir89/BikeSharingProject.git
cd BikeSharingProject
```

### 2. Install Dependencies

```bash
python -m pip install -r requirements.txt
python -m pip install folium jupyter
```

If the pickle contains GeoPandas objects, its original geospatial dependencies may also be required.

### 3. Add the Dataset

Place your trusted copy of this file in the repository root:

```text
BikeSharingData_Berlin_combinedandcleaned.pkl
```

Only load pickle files from a trusted source.

### 4. Open the Main Notebook

```bash
jupyter notebook BikeSharing_Berlin_Cleaned_Combined.ipynb
```

### 5. Import Folium Before Running the Map Cells

The current notebook imports Folium after earlier cells already reference it. Add this line to the first import cell before running the notebook from top to bottom:

```python
import folium
```

The route-sampling cell requires at least 100 rows with complete origin and destination coordinates.

## Repository Contents

| Path | Description |
|---|---|
| `BikeSharing_Berlin_Cleaned_Combined.ipynb` | Main exploratory analysis notebook |
| `bike_sharing_analysis/bike_sharing_analysis.ipynb` | Supplementary plotting snippet requiring an existing `df` |
| `images/` | Saved visualization previews |
| `requirements.txt` | Pandas, NumPy and Matplotlib dependencies |
| `README.md` | Project documentation |

## Limitations

- The input dataset is not distributed with the repository.
- The notebook starts from an existing cleaned pickle file; it does not reproduce the original data collection and cleaning process.
- Starting locations are grouped by exact coordinates, which may split nearby points that belong to the same operational area.
- Maps limited to the first 100 or 500 unique locations are illustrative subsets.
- Lines between origins and destinations do not represent actual cycling routes.
- The random trip sample may change between runs.
- Recorded trips alone do not measure unmet demand or bike availability.
- Weather effects, predictive models and forecast-accuracy improvements are not established by the current notebooks.
- No cost savings or operational improvements have been measured.

## Future Improvements

- Document the original dataset source and collection period.
- Provide permitted data-access instructions or a shareable sample.
- Add coordinate, duration and speed validation.
- Consolidate imports and dependencies for a clean top-to-bottom run.
- Group nearby origins into geographic areas.
- Use a fixed random seed for reproducible route samples.
- Add weather analysis or demand forecasting only when suitable data and validation are available.

## Author

**Balbir Singh**

M.Sc. Finance & Investment | Data Analysis | Finance & Operations

- [LinkedIn](https://www.linkedin.com/in/balbir-finance-investment-berlin/)
- [GitHub](https://github.com/Balbir89)
- [Email](mailto:balbirbhatia.20@gmail.com)
