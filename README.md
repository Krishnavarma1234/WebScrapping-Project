# WebScrapping-Project
Bike Wala
This project is an automated web scraping tool designed to collect technical specifications and pricing details of motorcycles from popular Indian brands. Built using Python, it extracts real-time data directly from the web, cleans it up using regular expressions (Regex), and aggregates it into a single, structured dataset (DataFrame) for analysis.

Data Extraction: For every brand, the script searches the webpage HTML to pull out raw chunks of text containing:Bike NamesPricing InformationUser RatingsTechnical Specs (Engine displacement, Mileage, Power, and Weight)Smart Text Parsing

(Regex): Because technical specs are often clustered together in single sentences, the script uses Regular Expressions (Regex) to smartly isolate and extract exact metrics (like matching numbers followed by cc, kmpl, bhp, or kg). If a metric is missing, it safely replaces it with a blank value (NaN).

Data Aggregation & Structuring: It organizes the extracted lists into individual mini-tables for each brand, and then combines (concatenates) them all into one final, master DataFrame using the pandas library.

Quality Checks: At the very end, the script prints out data diagnostics, showing the final shape of the dataset, checking for missing values, and counting how many bikes were successfully extracted per brand.
