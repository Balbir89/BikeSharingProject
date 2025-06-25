BikeSharingProject

This repository contains cleaned and combined bike sharing data from Berlin.

Dataset

- File: `BikeSharingData_Berlin_combinedandcleaned.pkl`  
- Format: Python pickle file (.pkl)  
- Description: The data includes bike rental records, timestamps, station info, and weather data.

How to use

Load the `.pkl` file in Python using pandas or pickle.  
Example:

```python
import pandas as pd

data = pd.read_pickle('BikeSharingData_Berlin_combinedandcleaned.pkl')
print(data.head())


Project background
This project was completed using Google Colab, focusing on cleaning and combining bike sharing data to analyze usage patterns in Berlin.

Contact
For questions, contact: balbirbhatia.20@gmail.com

