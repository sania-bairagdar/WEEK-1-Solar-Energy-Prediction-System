# ☀️ **Cleaned Solar Power Generation Dataset**
This repository contains a cleaned and preprocessed Solar Power Generation Dataset prepared for machine learning-based solar energy prediction.
It includes environmental and weather parameters that influence solar power production, such as radiation, sunshine duration, temperature, and humidity.

# ℹ️ Original Dataset Information
| Detail            | Description                                             |
| ----------------- | ------------------------------------------------------- |
| **Source**        | Solar Prediction Dataset                                |
| **Purpose**       | Predict solar radiation based on environmental features |
| **Sampling Rate** | Periodic weather observations                           |
| **Total Records** | 32,000+ (after cleaning)                                |
| **File Type**     | CSV                                                     |


# 📊 Dataset Overview
| Column            | Description                        | Unit       |
| ----------------- | ---------------------------------- | ---------- |
| **Temperature**   | Ambient temperature                | °C         |
| **Pressure**      | Atmospheric pressure               | hPa        |
| **Humidity**      | Relative humidity                  | %          |
| **WindDirection** | Wind direction                     | degrees    |
| **Speed**         | Wind speed                         | m/s        |
| **TimeSunRise**   | Local sunrise time                 | hh:mm:ss   |
| **TimeSunSet**    | Local sunset time                  | hh:mm:ss   |
| **Radiation**     | Solar radiation intensity (Target) | W/m²       |
| **Date**          | Date of observation                | yyyy-mm-dd |
| **Time**          | Time of observation                | hh:mm:ss   |

# 🧹 Cleaning Steps Performed
Standardized Date and Time columns for consistent formatting and combined them into a single timestamp (Date-Hour(NMT)).
Dropped rows with missing, invalid, or duplicate timestamps to ensure temporal accuracy.
Converted all numeric columns (e.g., Temperature, Pressure, Humidity, WindDirection(Degrees), Speed, Radiation) to consistent float64 or int64 data types.
Replaced negative or unrealistic values in Radiation, Temperature, and other physical parameters with corrected estimates based on logical bounds.
Filled missing numeric entries using median or mode imputation to preserve data integrity.
Verified physical limits for weather-based parameters such as temperature (°C), humidity (%), wind speed (m/s), and radiation (W/m²).
Extracted temporal features — hour, day, and month — to enable time-based energy forecasting.
Normalized continuous features like radiation, temperature, and wind speed for improved model performance and faster convergence.
Detected and removed outliers using statistical thresholds (z-score / IQR-based filtering).
Ensured no duplicate or inconsistent rows remained after preprocessing.
Saved the cleaned dataset as SolarPrediction_cleaned.csv, ready for use in machine learning–based solar energy prediction and forecasting models.g

# 📦 Files Included
| File Name                              | Description                                                                                                                                             |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **solar_power_data_with_energy.csv**   | Final cleaned dataset containing all meteorological features and the derived target column **`EstimatedEnergy`**, ready for ML training and forecasting |
| **solar_energy_cleaning_script.ipynb** | Jupyter/Google Colab notebook used for data cleaning, preprocessing, and feature generation                                                             |
| **README.md**                          | Documentation file explaining dataset details, cleaning steps, and usage instructions                                                                   |
****

# ⚙️ Example Usage
import pandas as pd

Load the cleaned dataset
df = pd.read_csv('SolarPrediction_cleaned.csv')

Display dataset information
print("Dataset Shape:", df.shape)
print("\nColumn Names:", df.columns.tolist())

Preview the first few rows
print("\nSample Data:")
print(df.head())

Optional: check for any missing values
print("\nMissing Values per Column:")
print(df.isnull().sum())

# 🧠 Potential Use Cases
Solar energy production forecasting
Machine learning and AI modeling for renewable energy optimization
Correlation analysis between weather parameters and power generation
Time-series forecasting and environmental trend analysis
Smart grid and sustainability research projects

# 🏷️ Source
Original dataset collected from Solar Power Plant Monitoring Systems.
Cleaned and processed using Python (Pandas, NumPy, Scikit-learn) for educational and research purposes.

# 📜 License
This cleaned dataset is released for educational and research purposes only.
Please cite this repository and the original dataset source if used in publications or research.

# 🤝 Contributing
Contributions are welcome!
Feel free to fork this repository, create a branch, and submit a Pull Request with improvements, model experiments, or data visualizations.

# 👩‍💻 Author
Maintained by Sania Bairagdar
Computer Science Engineering Student
Demonstrating data cleaning, preprocessing, and solar energy prediction using machine learning
