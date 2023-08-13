Flight Data Scraper

A Python utility that scrapes live flight data and saves it to a CSV file. The script continuously fetches aircraft information from a local endpoint and logs the data with the current timestamp. It creates a new CSV file every day to segregate the data based on the date.

Features:
Fetches live aircraft data from http://192.168.1.107/ajax/aircraft.
Writes the data to a CSV file named with the current date, e.g., flight_data_2023-07-31.csv.
The CSV file is updated every 15 seconds with new aircraft data.
A new CSV file is created at the start of each day.
Handles exceptions gracefully and prints errors to the console.
CSV Format:
The CSV file is structured in the following format:


lat,lon,type,time
49.4897,-125.287797,B738,2023-07-31 00:05:40
...

Prerequisites:
Python 3.x
requests library (can be installed using pip install requests)
Usage:
Ensure the destination folder exists (default: /Users/viraf/csv).
Run the script using Python:

$ python your_script_name.py
Check the destination folder for the generated CSV file(s).
Customization:
You can change the url variable to point to a different endpoint if required.
Modify the downloads_folder variable to set a different path for the CSV files.
Adjust the time.sleep(15) line if a different scraping frequency is desired.


-----------------------------------------------------------------------------------------------------------------------------------






