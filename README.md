# house-prices-veri-analizi

# **Real Estate Data Analysis and Preprocessing**

This project involves the exploratory data analysis (EDA) and preprocessing of a real estate dataset. The goal is to understand the data, clean it, and prepare it for further analysis or modeling.

## **Dataset Overview**

The dataset contains information about real estate properties, including their location, price, property type, and other related attributes. Below are the main characteristics of the dataset:

- **Number of Rows**: 168,446  
- **Number of Columns**: 20  

### **Dataset Columns**

| Column Name       | Description                                         |
|--------------------|-----------------------------------------------------|
| `property_id`      | Unique identifier for each property                 |
| `location_id`      | Location identifier                                 |
| `page_url`         | URL of the property listing                        |
| `property_type`    | Type of property (e.g., Flat, House)               |
| `price`            | Price of the property                              |
| `location`         | Location of the property within the city           |
| `city`             | City where the property is located                 |
| `province_name`    | Province name                                      |
| `latitude`         | Latitude coordinates of the property               |
| `longitude`        | Longitude coordinates of the property              |
| `baths`            | Number of bathrooms                                |
| `area`             | Area size in Marla/Kanal                           |
| `purpose`          | Purpose of the listing (e.g., For Sale)            |
| `bedrooms`         | Number of bedrooms                                 |
| `date_added`       | Date when the property was listed                  |
| `agency`           | Real estate agency name                            |
| `agent`            | Real estate agent name                             |
| `Area Type`        | Type of area (e.g., Marla, Kanal)                  |
| `Area Size`        | Area size in numerical form                        |
| `Area Category`    | Area category based on size (e.g., 0-5 Marla)      |

---

## **Project Workflow**

### **1. Data Loading and Inspection**
- Load the dataset using **Pandas**.
- Inspect the dataset's structure, including dimensions and column data types.
- Check for missing values and their percentages.

### **2. Exploratory Data Analysis (EDA)**
EDA is performed to gain insights into the dataset. Steps include:
- **General Analysis**:
  - Viewing the first few rows (`head()`).
  - Basic statistics (`describe()`) and data types (`info()`).
- **Missing Data Analysis**:
  - Calculate the percentage of missing data in each column.
- **Visualization**:
  - **Distribution Analysis**: Visualize the distribution of numeric variables (e.g., `price`, `area`) using histograms and boxplots.
  - **Correlation Analysis**: Analyze relationships between numeric variables using a heatmap.
  - **Geographical Visualization**: Plot property locations using latitude and longitude.
- **Categorical Analysis**:
  - Analyze the frequency distribution of categorical variables (e.g., `property_type`, `city`, `purpose`).

### **3. Data Cleaning and Preprocessing**
- Handle missing values:
  - Fill missing values in numeric columns with the **mean** or **median**.
  - Fill missing values in categorical columns with the **mode**.
- Remove outliers:
  - Identify and remove outliers using the **IQR (Interquartile Range)** method.
- Drop unnecessary columns:
  - Columns such as `page_url`, `property_id`, and `location_id` are removed as they are not relevant for analysis.
- Convert data types:
  - Ensure proper data types (e.g., convert `price` and `area` to `float`).
- Standardize area values:
  - Extract numeric values from the `area` column.

### **4. Saving the Processed Dataset**
- Save the cleaned and processed dataset as `cleaned_dataset.csv` for further use.

---

## **Setup Instructions**

1. Clone this repository or download the project files.
2. Ensure you have Python installed on your system.
3. Install the required libraries using:

   ```bash
   pip install pandas matplotlib seaborn
4. Run the Jupyter Notebook or Python script containing the code.
