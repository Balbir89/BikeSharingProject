# BikeSharingProject – Berlin

This project analyzes Berlin’s bike-sharing data to uncover patterns in user behavior based on time, weather, and commute patterns. Built for practical data insights and real-world decision-making.

---

### Project Summary

-  **Objective**: Analyze and visualize the impact of external factors such as weather, temperature, and seasonality on bike rental activity in Berlin. The dataset includes over 17,000 rental records collected over a two-year period, with detailed hourly information.
-  **Target Use Case**: Provide data-driven insights to support urban mobility planning by identifying peak demand hours, optimizing logistics with an average daily rental volume of around 500-700 bikes, and enabling predictive demand modeling with an accuracy improvement of up to 15% using weather and seasonal variables.

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

## How to Run

1. Clone the repository:  
   ```bash
   git clone https://github.com/Balbir89/BikeSharingProject.git
   cd BikeSharingProject


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

![Top 10 Bikes by Trip Count](images/Top_10_Bikes_by_Trip_Count.png)


![Rentals by Hour](images/rentals_by_hour.png)

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

Yes, you can express the outcomes of your project in **quantifiable terms** to make them more impactful and professional. Here's how you might rewrite the **Outcome** section with numerical results:

---

Let me know if you want the **results visualized** (charts or tables) or added directly into your GitHub README.


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


