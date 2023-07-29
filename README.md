# Car Sales Report Generator

This Python script analyzes car sales data and generates a comprehensive report summarizing the results. The script loads data from a JSON file, processes the information, and produces both a PDF report and an email containing the report as an attachment.

## Prerequisites

- Python 3.x

## Setup

1. Clone the repository or download the script to your local machine.

```bash
git clone https://github.com/your-username/car-sales-report.git
cd car-sales-report
```

2. Install the required Python libraries.

```bash
pip install emails
pip install json
pip install locale
pip install reports
```

## Usage

1. Ensure that you have the car sales data stored in a valid JSON file (e.g., `car_sales.json`) in the same directory as the script. The JSON file should have the following format:

```json
[
  {
    "id": 1,
    "car": {
      "car_make": "Toyota",
      "car_model": "Corolla",
      "car_year": 2022
    },
    "price": "$25000.00",
    "total_sales": 50
  },
  {
    "id": 2,
    "car": {
      "car_make": "Honda",
      "car_model": "Civic",
      "car_year": 2021
    },
    "price": "$23000.00",
    "total_sales": 45
  },
  ...
]
```

2. Run the script with the following command:

```bash
python car_sales_report.py
```

3. The script will process the data and generate a summary of the car sales, including the car that generated the most revenue, the car with the highest sales, and the most popular car year.

4. A PDF report named `cars.pdf` will be generated in the `/tmp` directory, containing detailed information about the sales summary for the last month.

5. An email will be sent to the specified recipient, containing the same sales summary PDF report as an attachment.

## Customize

If you wish to use a different JSON file for data or change the email settings, you can modify the following lines in the script:

- To change the JSON data file path:

```python
data = load_data("path/to/your/car_sales.json")
```

- To update the email settings:

```python
sender = "automation@example.com"
recipient = "user@example.com"
subject = "Sales summary for last month"
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- This script uses the `emails` and `reports` libraries to handle email and PDF report generation, respectively.
