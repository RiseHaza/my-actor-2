[My Actor 2](https://apify.com/moving_beacon-owner1/my-actor-2?fpr=data)

# Hotel Data Scraper

This project is a robust web scraping solution built with Playwright and Python, designed to extract detailed hotel data from various hotel booking pages. The tool scrapes information such as hotel names, check-in/check-out dates, and prices, and exports the data into an Excel file. Additionally, it integrates seamlessly with Apify for storing the extracted data in a dataset for further processing.

## Key Features

- **Accurate Data Extraction**: Scrapes hotel names, check-in/check-out dates, and prices for any provided hotel URL.
- **Date Navigation**: Automatically navigates between calendar months to extract data for the required period.
- **Excel Export**: Saves the extracted data to an Excel file for easy sharing and analysis.
- **Apify Integration**: Pushes the extracted data to an Apify dataset, enabling cloud-based storage and further processing.
- **Error Handling and Retries**: The scraper automatically retries failed attempts to ensure consistent data extraction.
- **Price Formatting**: Cleans and formats prices, removing unnecessary characters such as currency symbols.

## Benefits for You

- **Easy Data Access**: Automatically extracts the data you need from multiple hotel booking pages.
- **Time-Saving**: Eliminates manual data collection, saving time and improving efficiency.
- **Scalable**: Can handle multiple hotel URLs in one run, ideal for large-scale data collection.
- **Reliable**: Includes retry mechanisms to handle network errors and page loading issues.
- **Flexible**: Can be easily customized to scrape additional data or integrate with other systems.

1. **Configure Input Data**:

Provide a list of hotel URLs in the `startUrls` key of the input. Here's an example:

```
{
  "startUrls": [
    "https://www.example.com/hotel1",
    "https://www.example.com/hotel2"
  ]
}
```
2. **Run the Scraper**:

Once the setup is complete, run the scraper
The script will:

- Extract data from each provided hotel URL.
- Save the data to an Excel file (named with a timestamp for easy identification).
- Push the data to the Apify dataset for cloud-based storage.

## Output

- **Excel File**: The extracted data will be saved in an Excel file (`hotel_data_<timestamp>.xlsx`).
- **Apify Dataset**: All the extracted data will be pushed to your Apify dataset for further processing or storage.

## Customization

- You can adjust the `extract_dates_and_prices` function to scrape additional information, such as amenities or room details.
- Modify the `startUrls` list to include any hotel URLs you wish to scrape.