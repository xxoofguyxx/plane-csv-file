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


Flight Data Visualization
This is an HTML utility that fetches flight data from a CSV file and displays it in a table format. The CSV file's name is dynamically generated based on the current date (PST timezone). This table will also provide direct links to Google, Wikipedia, and OpenStreetMap based on the data.

Features:
Dynamic CSV Path Generation: The script fetches data from a CSV file named with the current date in PST timezone, e.g., flight_data_2023-07-31.csv.
Comprehensive Table View: Data is displayed in a table format with columns: Latitude, Longitude, Type, Time, Google Search link, Wikipedia link, and OpenStreetMap link.
Interactive Links:
Google Search: Clicking this link searches the aircraft type on Google.
Wikipedia Page: This link takes you to the Wikipedia page of the specific aircraft type.
OpenStreetMap: If the latitude and longitude data are present, this link will direct you to the aircraft's location on OpenStreetMap.
Adaptive Rendering: In case latitude and longitude data are absent, the OpenStreetMap link will display as 'N/A'.

Usage:
Place this HTML file on a server or open it directly in a web browser.
Ensure that the CSV file (flight_data_YYYY-MM-DD.csv) is accessible from the same location or provide the correct path to the file.
Open the HTML file in a web browser. The script will automatically fetch the data from the CSV file and render the table.

Customization:
To fetch data from a different location or with a different naming convention, modify the csvFilePath variable.
Adjustments to the table structure or additional columns can be made by editing the script within the <script> tags.

Dependencies:
The utility assumes that the CSV file exists and is named based on the date in PST timezone.
No external libraries or frameworks are required, as this utility uses vanilla JavaScript.
