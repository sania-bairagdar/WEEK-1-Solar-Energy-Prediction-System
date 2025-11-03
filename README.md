☀️ Cleaned Solar Power Generation Dataset
This repository contains a cleaned and preprocessed Solar Power Generation Dataset prepared for machine learning-based solar energy prediction.
It includes environmental and weather parameters that influence solar power production, such as radiation, sunshine duration, temperature, and humidity.

ℹ️ Original Dataset Information
Source: Solar Plant Observation Logs
Time Period: Several months of hourly data collection
Sampling Rate: 1 hour
Number of Measurements: 1,801 records (after cleaning)
Target Variable: Estimated solar energy output (EstimatedEnergy)

📊 Dataset Overview
Column	Description	Unit
Date-Hour(NMT)	Combined date and time of observation	—
WindSpeed	Wind speed at the solar plant site	m/s
Sunshine	Duration of sunlight exposure	hours
AirPressure	Atmospheric pressure during the reading	hPa
Radiation	Solar radiation intensity	W/m²
AirTemperature	Ambient air temperature	°C
RelativeAirHumidity	Relative humidity in the air	%
hour	Extracted hour from timestamp	—
day	Extracted day of the month	—
month	Extracted month	—
EstimatedEnergy	Derived solar power output value	kWh

🧹 Cleaning Steps Performed
Combined and standardized Date and Time into a single Date-Hour(NMT) column.
Dropped rows with missing or invalid timestamps.
Replaced negative values in Radiation and AirTemperature with realistic corrected values.
Filled missing numeric fields using median or mode imputation.
Removed constant or redundant columns (SystemProduction, etc.).
Converted all numeric columns to proper data types (float64 or int64).
Extracted hour, day, and month for time-based analysis.
Normalized Sunshine within the range 0–12 hours.
Created a new target feature EstimatedEnergy using Radiation, Sunshine, and AirTemperature.
Removed outliers and ensured no duplicate rows remained.
Saved the final cleaned file ready for ML model training and forecasting.

📦 Files Included
File	Description
solar_power_data_with_energy.csv	Dataset containing the derived target (EstimatedEnergy)
solar_energy_cleaning_script.ipynb	Python/Colab notebook used for data cleaning and preparation
README.md	This documentation file

⚙️ Example Usage
import pandas as pd
# Load cleaned dataset
df = pd.read_csv('solar_power_data_fixed_datetime.csv', parse_dates=['Date-Hour(NMT)'])
# Display info
print(df.info())
print(df.head())

🧠 Potential Use Cases
Solar energy production forecasting
Machine learning and AI modeling for renewable energy optimization
Correlation analysis between weather parameters and power generation
Time-series forecasting and environmental trend analysis
Smart grid and sustainability research projects

🏷️ Source
Original dataset collected from Solar Power Plant Monitoring Systems.
Cleaned and processed using Python (Pandas, NumPy, Scikit-learn) for educational and research purposes.

📜 License
This cleaned dataset is released for educational and research purposes only.
Please cite this repository and the original dataset source if used in publications or research.

🤝 Contributing
Contributions are welcome!
Feel free to fork this repository, create a branch, and submit a Pull Request with improvements, model experiments, or data visualizations.

👩‍💻 Author
Maintained by Sania Bairagdar
Computer Science Engineering Student
Demonstrating data cleaning, preprocessing, and solar energy prediction using machine learning
