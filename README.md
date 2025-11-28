# 📉 Exchange Rate Scraper - SBS Peru

This project is an automation tool developed in **Python** to extract the exchange rate history (USD) directly from the official portal of the **Superintendence of Banking, Insurance and AFP (SBS)** of Peru.

The script automates web navigation, queries by date ranges, and extracts structured data, exporting the results to a CSV file ready for analysis.

## 🚀 Features

* **Browser Automation:** Uses `Selenium` and `undetected-chromedriver` to simulate human interaction and avoid simple blocking mechanisms.
* **Date Range Search:** Allows defining a start and end date to iterate day by day.
* **Error Handling:** Includes retries and random wait times to maintain connection stability.
* **Data Export:** Generates a clean `TipoCambio_CompraVenta.csv` file with the columns: Date, Buy (Compra), and Sell (Venta).

## 🛠️ Tech Stack

* **Python 3.13.7**
* [Selenium](https://www.selenium.dev/): For browser automation.
* [Undetected Chromedriver](https://github.com/ultrafunkamsterdam/undetected-chromedriver): An optimized version of the Chrome driver to bypass bot detection.
* [Pandas](https://pandas.pydata.org/): For data manipulation and export.

## 📋 Prerequisites

You need to have **Google Chrome** installed on your system, as the script uses its driver.

## ⚙️ Installation

1. Clone this repository:
```bash
git clone https://github.com/MarcOBL012/Exchange-Rate-Scraper-SBS-Peru.git
```


2. Install the necessary dependencies:

```Bash
pip install pandas selenium undetected-chromedriver
```

## ▶️ Usage
1. Open the Scraping_SBS.py file.
2. In the main() function, modify the start and end dates according to your needs:
```
# Example: Query from November 3rd to November 25th, 2025
df_sbs = obtener_tipo_cambio('2025-11-03', '2025-11-25')
```
3. Run the script:

```Bash
python Scraping_SBS.py
```
4. Once finished, you will find the TipoCambio_CompraVenta.csv file in the same folder.
