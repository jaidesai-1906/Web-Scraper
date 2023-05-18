# Web Scraper using Selenium and BeautifulSoup

This script is a web scraper that uses Selenium WebDriver for browser automation and BeautifulSoup4 for parsing HTML and extracting the necessary information. It's designed to read input from a CSV file, navigate to specific webpages according to the inputs, scrape the content of these pages, and then write the scraped data into an output CSV file.

## Getting Started

### Prerequisites

Before running the script, please ensure that you have:

- Python 3.6 or later: You can download it from the official site - https://www.python.org/downloads/
- ChromeDriver: This is needed for Selenium to interact with the Chrome browser. Download the version compatible with your system and your installed Chrome version from here - https://sites.google.com/a/chromium.org/chromedriver/downloads
- Tor Proxy (optional): If you want to use a proxy, you need to set up Tor Proxy.

### Installation

1. Clone the repository or download the Python script.
2. Install the required Python packages. You can do this by navigating to the project directory in your terminal and running the following command:
```bash
pip install -r requirements.txt
```

## Usage
Firstly, update the config dictionary in the second cell of the Jupyter Notebook to match your requirements. Here's a quick rundown of the keys in this dictionary:

- input_csv: The path to the input CSV file.
- output_csv: The path where the output CSV file will be saved.
- start_url: The initial URL that the browser will navigate to. The {} placeholder will be replaced with the email/id read from the CSV file.
- target_url: The URL of the page from which data will be scraped.
- chromedriver_path: The path to your ChromeDriver executable.
- tor_proxy: The address of the Tor proxy you want to use.

The script will read each email from the input CSV, navigate to the start URL, then navigate to the target URL, and scrape the page's body content. It'll then write the email and scraped content to the output CSV. If it encounters an error for any email, it'll print an error message and continue with the next email.

After all emails have been processed, the browser will be closed automatically.