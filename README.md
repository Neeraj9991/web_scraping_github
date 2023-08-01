# Web Scraping GitHub Topics

## Introduction

This project is a Python script designed to perform web scraping on GitHub topics. It extracts information about the top repositories for various topics on GitHub and saves the data in a structured format for further analysis. The script utilizes the "requests" and "Beautiful Soup" libraries for web scraping and "Pandas" for data manipulation.

## Dependencies

- Python 3.x
- `requests`: To send HTTP requests and fetch web page data.
- `BeautifulSoup`: To parse and navigate HTML data.
- `Pandas`: To store and manipulate the extracted data in a tabular format.
- `os`: To handle file and directory operations.

## Getting Started

1. Clone the repository to your local machine.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Open the Jupyter notebook `web_scraping_github.ipynb` to run the web scraping script.

## How It Works

The web scraping process is divided into two main parts:

1. **Extracting GitHub Topics**
   - The `get_topics_page(topics_url)` function fetches the GitHub topics page.
   - The `get_topic_details(doc)` function extracts topic details such as title, description, and URL.
   - The `scrape_topics()` function assembles the extracted data into a Pandas DataFrame.

2. **Getting Repositories from Extracted Topics**
   - The `get_repo_info(h3_tags, star_tags)` function extracts repository information.
   - The `get_topic_repos(topic_doc)` function scrapes and stores the repositories' details for a specific topic.
   - The `scrape_topics_repos()` function executes the entire web scraping process for all topics.

## Usage

To run the web scraping script:

1. Ensure you have Python 3.x installed on your system.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Open the Jupyter notebook `web_scraping_github.ipynb`.
4. Execute each cell to perform the web scraping process.
5. The script will create a "data" directory and save CSV files containing information about top repositories for different topics.

## Future Scope

- Allow users to input specific topics or filters for customized data extraction.
- Error Handling and Robustness : Handle scenarios such as connection timeouts, invalid responses, or unexpected HTML structure gracefully, ensuring the script continues to run smoothly under various conditions.
- Keyword Extraction: Extract key topics and programming language used from repository descriptions

## Contribution

Contributions to this project are welcome. If you encounter any issues or have ideas for improvements, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

