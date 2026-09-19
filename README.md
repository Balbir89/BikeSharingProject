


# Bike-Sharing Trip Analysis — Berlin

Exploratory analysis of Berlin bike-sharing trip records using Python, Pandas, Matplotlib and Folium.

This independent portfolio project explores when trips occur, where they start, which bikes are used most frequently and how trip characteristics vary.

[View Main Notebook](BikeSharing_Berlin_Cleaned_Combined.ipynb) · [View Visualizations](images) · [Dataset Source](https://zenodo.org/records/10046531)

## Project Objective

Explore trip activity through time-based analysis and geographic visualization to support questions about bike usage and fleet allocation.

Key questions:

- How does recorded trip volume vary by day and hour?
- Which starting coordinates have the most trips?
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
| Folium | Interactive maps, heatmaps and marker clusters |
| Jupyter Notebook | Code, explanations and visual outputs |

## Dataset Source

Kaiser, Silke Kirstin (2023). *Bike-sharing data Berlin from Nextbike and Call-a-Bike for 2019 and 2022*. Zenodo.

**DOI:** https://doi.org/10.5281/zenodo.10046531

The published dataset covers:

- **April–December 2019:** Nextbike and Call-a-Bike data provided by City Lab Berlin.
- **June–December 2022:** web-scraped Nextbike data.

The source includes raw bike-sharing data and a routed, cleaned version. These are separate collection periods, not continuous coverage from 2019 to 2022.

### Input File

The main notebook loads:

`BikeSharingData_Berlin_combinedandcleaned.pkl`

This exact filename is available in the Zenodo record. The file is approximately **276.7 MB** and is hosted externally.

### Download Instructions

1. Open the [Zenodo dataset page](https://zenodo.org/records/10046531).
2. Download `BikeSharingData_Berlin_combinedandcleaned.pkl`.
3. Place it in the repository root alongside the main notebook.

### Fields Used in the Analysis

| Field | Use |
|---|---|
| `time_origin` | Trip date and hour |
| `lat_origin`, `long_origin` | Starting coordinates |
| `lat_destination`, `long_destination` | Destination coordinates |
| `bikeid` | Trip counts per bike |
| `speed_kmh` | Average recorded speed |
| `duration_betweenorigindestination` | Trip-duration analysis |

The notebook divides the duration field by 60 to express duration in minutes. This assumes the source values are in seconds and should be checked against the dataset documentation.

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
- Trip-duration distribution

### 5. Map Trip Locations

Use Folium to create:

- A heatmap of trip origins
- A clustered map of up to 500 unique origin locations
- A map of up to 100 unique starting locations
- Straight-line connections for a random sample of 100 trips

The starting-location map is exported as `starting_locations_map.html` when its notebook cell runs.

## Selected Visualizations

### Top 10 Bikes by Trip Count

Compare recorded trip counts for the ten most frequently used bikes.

![Top 10 Bikes by Trip Count](images/Top%2010%20Bikes%20by%20Trip%20Count.png)

### Clustered Map of Trip Origins

Explore a subset of starting locations using clustered map markers.

![Clustered Map of Trip Origins](images/Clustered%20Marker%20Map%20of%20Origins%20Goal.png)

### Top 10 Starting Locations

Compare the most frequent starting coordinate pairs in the dataset.

![Top 10 Starting Locations](images/Top%2010%20starting%20locations%20plot%20generated%20successfull.png)

## Potential Operational Uses

| Analysis | Question It Can Support |
|---|---|
| Daily and hourly trip counts | When does recorded activity increase or decrease? |
| Origin-location analysis | Where is recorded usage concentrated? |
| Trip counts per bike | Which bikes have particularly high recorded usage? |
| Speed and duration distributions | Which observations warrant further investigation? |
| Geographic visualizations | Where could more detailed fleet-allocation analysis be useful? |

These are potential applications, not measured improvements in operating costs, service quality or fleet performance.

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

If the pickle contains GeoPandas objects, the corresponding geospatial dependencies may also be required.

### 3. Download the Dataset

Download `BikeSharingData_Berlin_combinedandcleaned.pkl` from:

https://zenodo.org/records/10046531

Place the file in the repository root. Only load pickle files from a trusted source.

### 4. Open the Main Notebook

```bash
jupyter notebook BikeSharing_Berlin_Cleaned_Combined.ipynb
```
### 5. Run the Notebook

Run the cells from top to bottom to generate the charts and maps. Folium is imported in the first code cell.

The route-sampling cell requires at least 100 rows with complete origin and destination coordinates. Map rendering may be resource-intensive for large datasets.

### 6. Run the Analysis

Run the notebook cells in order to inspect the data and generate charts and maps.

The route-sampling cell requires at least 100 rows with complete origin and destination coordinates. Map rendering may be resource-intensive for large datasets.

## Repository Contents

| Path | Description |
|---|---|
| `BikeSharing_Berlin_Cleaned_Combined.ipynb` | Main exploratory analysis notebook |
| `bike_sharing_analysis/bike_sharing_analysis.ipynb` | Supplementary plotting snippet requiring an existing `df` |
| `images/` | Saved visualization previews |
| `requirements.txt` | Pandas, NumPy and Matplotlib dependencies |
| `README.md` | Project documentation |

The input dataset is downloaded separately from Zenodo.

## Scope and Limitations

- The analysis starts from an existing cleaned dataset; it does not reproduce the original collection and cleaning process.
- The source covers selected months in 2019 and 2022. Differences in collection period and provider coverage should be considered before comparing activity.
- Starting locations are grouped by exact coordinates, which may separate nearby points belonging to the same operational area.
- Maps limited to the first 100 or 500 unique locations show illustrative subsets.
- Lines connecting origins and destinations do not represent actual cycling routes.
- The random trip sample may change between runs.
- Recorded trip counts alone do not measure unmet demand, bike availability or market-wide usage.
- Speed and duration values require validation before operational interpretation.
- The current notebooks do not establish weather effects, predictive-model performance or forecast improvements.
- No business cost savings or operational improvements have been measured.

## Future Improvements

- Include all required dependencies in requirements.txt and verify execution from a fresh environment.
- Add checks for missing values, duplicate records, coordinates, speed and duration.
- Report the loaded dataset's row count, date range and provider coverage.
- Analyze collection periods and providers separately.
- Group nearby origins into geographic areas.
- Use a fixed random seed for reproducible trip samples.
- Export interactive maps for easier viewing.
- Add weather analysis or demand forecasting when suitable data and validation are available.

## Attribution

Dataset credit belongs to the creators and providers identified in the [Zenodo record](https://doi.org/10.5281/zenodo.10046531).

This repository presents an independent analysis of that dataset. Refer to the source record for dataset reuse terms.

## Author

**Balbir Singh**

M.Sc. Finance & Investment | Data Analysis | Finance & Operations

- [LinkedIn](https://www.linkedin.com/in/balbir-finance-investment-berlin/)
- [GitHub](https://github.com/Balbir89)
- [Email](mailto:balbirbhatia.20@gmail.com)
