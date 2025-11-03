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
Standardized Date and Time columns for uniform formatting
Dropped rows with missing or invalid timestamps
Replaced negative or unrealistic values in Radiation and Temperature with corrected estimates
Filled missing numeric entries using median or mode imputation
Converted all numeric features to consistent float64/int64 data types
Extracted hour, day, and month from timestamp data for temporal analysis
Normalized solar radiation and other continuous features for improved model performance
Detected and removed outliers and duplicate rows
Verified logical physical limits for temperature, humidity, wind speed, and radiation
Saved the cleaned dataset as SolarPrediction_cleaned.csv, ready for machine learning model training and solar energy forecasting

# 📦 Files Included
File	Description
| File Name                              | Description                                                                                                                                             |
| -------------------------------------- 
| **solar_power_data_with_energy.csv**   | Final cleaned dataset containing all meteorological features and the derived target column **`EstimatedEnergy`**, ready for ML training and forecasting |
| **solar_energy_cleaning_script.ipynb** | Jupyter/Google Colab notebook used for data cleaning, preprocessing, and feature generation                                                             |
| **README.md**                          | Documentation file explaining dataset details, cleaning steps, and usage instructions                                              

# ⚙️ Example Usage
import pandas as pd
 Load cleaned dataset
df = pd.read_csv('solar_power_data_fixed_datetime.csv', parse_dates=['Date-Hour(NMT)'])
 Display info
print(df.info())
print(df.head())

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
