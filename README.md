# Amazon-Web-scraping-Project
Webscraping with python project.This project demonstrates how to scrape product information from an Amazon webpage using Python. The scraped data includes product images, titles, ratings, and prices, which are then saved into JSON and CSV files for further analysis.

## Introduction

The goal of this project is to extract product data from an Amazon webpage. This involves parsing the HTML content of a saved Amazon page, extracting relevant product details, and saving the extracted data into JSON and CSV files.

## Installation

To run this project, you need to have Python installed on your system along with the following libraries:

- BeautifulSoup
- pandas

## Usage
Save the HTML content of an Amazon search result page to your local system.
Update the file path in the script to point to your saved HTML file.
Run the script to scrape the data and save it in JSON and CSV formats.

## Detailed Steps
Importing Libraries: The script imports necessary libraries including BeautifulSoup for parsing HTML, json for handling JSON data, csv for handling CSV files, and pandas for data manipulation and analysis.

Reading HTML Content: The script reads the HTML content from a local file containing the saved Amazon search results page.

Parsing HTML with BeautifulSoup: The HTML content is parsed using BeautifulSoup to create a soup object that allows for easy navigation and data extraction from the HTML structure.

Finding Relevant Divs: The script searches for all div elements with a specific class that indicates product listings. These div elements contain the information of interest.

Extracting Data: The script iterates over each product div and extracts relevant information such as the product image link, title, rating, and price. This information is stored in a dictionary and appended to a list.

Saving Data to JSON: The extracted data is saved into a JSON file for structured storage and easy access.

Loading Data into Pandas DataFrame: The JSON data is loaded into a pandas DataFrame for further manipulation and analysis.

Saving Data to CSV: The DataFrame is saved into a CSV file, providing a tabular representation of the scraped data that is easy to view and analyze.

## Function Explanations

# BeautifulSoup
BeautifulSoup(html_content, 'html.parser'): This creates a BeautifulSoup object from the HTML content, allowing for easy navigation and data extraction from the HTML structure.

# find_all
soup.find_all('div', class_="..."): This function searches for all div elements in the HTML content that have the specified class. It returns a list of all matching elements.

# find
div.find('img', class_='s-image s-image-optimized-rendering'): This function searches within a specific div element for an img tag with the specified class. It returns the first matching element or None if no match is found.

div.find('span', class_='a-size-base-plus a-color-base a-text-normal'): Similar to the above, this searches for a span tag with the specified class within a specific div element.

div.find('span', class_='a-icon-alt'): Searches for a span tag with the specified class within a specific div element.

div.find('span', class_='a-price-whole'): Searches for a span tag with the specified class within a specific div element.

# JSON Handling
json.dump(data, json_file, ensure_ascii=False, indent=4): This function writes the extracted data to a JSON file. The ensure_ascii=False parameter ensures that non-ASCII characters are preserved, and indent=4 makes the output more readable by indenting nested structures by four spaces.

# Pandas
pd.read_json('amazon_data.json'): This function reads the JSON data into a pandas DataFrame, allowing for easy data manipulation and analysis.

df_csv.to_csv(output_csv_path, index=False): This function writes the DataFrame to a CSV file. The index=False parameter prevents pandas from writing row indices to the file.
