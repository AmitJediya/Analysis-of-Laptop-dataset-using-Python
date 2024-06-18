# Analysis of Laptop dataset using Python

This project analyzes and cleans a dataset containing laptop specifications to gain insights into factors influencing price and potentially predict laptop prices.

## Project Overview

The goal of this project is to understand the relationship between laptop features (brand, type, specifications) and their prices. We clean and preprocess the data, conduct exploratory data analysis (EDA), and prepare the groundwork for potential price prediction modeling.

## Data Cleaning and Preparation

The dataset `laptopData.csv` is loaded using pandas. Initial steps involve:

- Removing unnecessary columns (e.g., `Unnamed: 0`)
- Handling missing values through deletion (given their consistency across rows)
- Transforming columns:
  - `Inches`: Converted to numeric from object, after handling anomalies ("?")
  - `ScreenResolution`: Derived new features:
    - `MyScreenRes`: Extracts resolution (e.g., "2560x1600")
    - `X_res` and `Y_res`: Numerical pixel counts
    - `Total_Pixels`: Total pixel count
    - `PPI`: Pixels Per Inch (PPI) calculation
    - `IsTouchScreen`: Boolean indicating touchscreen presence
  - `Cpu`: Extracted `Cpu_Company` and `Cpu_SpeedNum` (GHz in numeric format)
  - `Ram`: Converted to numeric from object
  - `Memory`: 
    - `MultiStorage`: Indicates the number of storage devices (SSD, HDD, Flash, etc) 
    - Derive a new feature `Primary_Storage_GB` which converts storage type to number (in GB) 
  - `Gpu`: Extracted `Gpu_Company`
  - `Weight`: Converted to numeric from object


## Exploratory Data Analysis (EDA)

Key visualizations and analyses performed:

- Distribution of categorical variables (e.g., screen resolutions, CPU companies)
- Impact of touchscreen on average price and PPI
- Average CPU speed by company
- Average RAM by company and laptop type

 
