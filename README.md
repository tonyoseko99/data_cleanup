# Data Cleaning and Analysis Project

This project is focused on cleaning and analyzing a dataset containing faculty information. The dataset may have inconsistencies, missing data, and other issues that need to be addressed before performing any meaningful analysis.

## Project Structure

The project is organized into the following directories and files:

- `code/`: Contains the Python script for data cleaning and analysis.
  - `data.py`: The main script that loads, cleans, and analyzes the dataset.
- `Data/`: Contains the raw data file.
  - `SIS_Faculty-List.xlsx`: The original dataset in Excel format.
- `reports/`: Contains the output reports and cleaned data.
  - `Result_cleaned.xlsx`: The cleaned dataset in Excel format.
  - `Result_cleaned.csv`: The cleaned dataset in CSV format.
  - `Report.csv`: A summary report of the cleaned data.

## Data Cleaning and Analysis Steps

1. **Loading the Data**: The dataset is loaded from the Excel file (`SIS_Faculty-List.xlsx`) using pandas.

2. **Data Cleaning**:
   - Handling Missing Data: Missing values in the 'Location' column are replaced with 'Unknown,' and rows with missing 'Reports To' values are removed.
   - Value Standardization: The 'Location' column is cleaned by removing leading/trailing spaces and capitalizing the first letter. The 'Join Date' column is converted to datetime format, handling invalid entries. The 'Highest Qualification' column is standardized using a custom function.

3. **Duplicate Data Removal**: Duplicate rows based on the 'ID' column are identified and removed from the dataset.

4. **Saving Cleaned Data**: The cleaned dataset is saved both in Excel and CSV formats for further analysis.

5. **Generating a Report**: A summary report of the cleaned data is generated and saved as 'Report.csv' in the 'reports/' directory.

6. **Data Type Standardization**: The script checks for data types in columns and provides recommendations for type standardization if necessary.

## How to Use

1. Clone this repository to your local machine.

2. Create a virtual environment and activate it.

    #### Linux / MacOS 
    ``` bash
    python -m venv venv
    source venv/bin/activate
    ```
    #### Windows
    ``` bash
    python -m venv venv
    venv\Scripts\activate
    ```

3. Install the required dependencies by running:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the script:

   ```bash
    python3 code/data.py
    ```

5. The cleaned dataset will be saved in the 'reports/' directory as 'Result_cleaned.xlsx' and 'Result_cleaned.csv'. The summary report will be saved as 'Report.csv' in the same directory.

## Dependencies

- Python 3.8.5
- pandas 1.2.4
- numpy 1.20.3
- openpyxl 3.0.7

## License

This project is licensed under the terms of the MIT license. See [LICENSE](LICENSE) for more details.
