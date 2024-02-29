# File Format Converter

## Overview

The objective of this project is to develop a solution to efficiently convert CSV files obtained from a MySQL database into JSON files. JSON format is preferred for downstream applications due to its flexibility and ease of use.

## Data Model Details

The data model consists of CSV files extracted from the MySQL database. These CSV files contain structured data that needs to be transformed into JSON format.

## Design

The design of the solution involves setting up a Python project to handle the conversion process. The core logic utilizes Pandas library to convert CSV files into DataFrames and then into JSON format. Exception handling is implemented to ensure robustness of the application.

### Setup Instructions

1. **Setup the Project Using VSCode:**
   - Ensure that you have set up a virtual environment for the project using tools like `venv`.
   - Install project dependencies listed in `requirements.txt`.
   - Deploy the application with the core logic implemented.

2. **Run the Project:**
   - After setting all the required environment variables, run the project to initiate the conversion process.

3. **Exception Handling:**
   - Implement appropriate exception handling mechanisms to handle errors gracefully.

### Validation Steps

1. **Data Conversion Verification:**
   - Check whether the data in the files has been converted properly from CSV to JSON format.
   - Verify that the target folder has been created and populated with JSON files.
   - Confirm that the schema structure was accurately reflected from the CSV files (Refer to `schemas.json`).
   
2. **Record Count Verification:**
   - Take the count of records in the original CSV files and compare it to the number of records in the generated JSON files.

```python
import pandas as pd

# Read orders JSON File using Pandas
orders_data_json = pd.read_json('data/retail_db/orders_json/part-00000', lines=True)
# Count rows
orders_data_json.count()

# Read order_items JSON File using Pandas
order_items_data_json = pd.read_json('data/retail_db/order_items_json/part-00000', lines=True)
# Count rows
order_items_data_json.count()
```

## Technologies Used

- Programming Language: Python
- Pandas: For Converting CSV to Dataframe and then Dataframe into JSON.

## README

### How to Use

1. Clone the repository:

   ```bash
   git clone https://github.com/your_username/file-format-converter.git
   ```

2. Navigate to the project directory:

   ```bash
   cd file-format-converter
   ```

3. Set up a virtual environment:

   ```bash
   python -m venv venv
   ```

4. Activate the virtual environment:

   - On Windows:

     ```bash
     venv\Scripts\activate
     ```

   - On macOS and Linux:

     ```bash
     source venv/bin/activate
     ```

5. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

6. Set environment variables (if necessary).

7. Run the project:

   ```bash
   python main.py
   ```

### Additional Notes

- Make sure to configure the input and output paths in the code according to your file locations.
- Ensure that the required permissions are set for reading and writing files.

## Contributors

- [Shrey Agrawal](https://github.com/shrey1002)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
