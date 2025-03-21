# DataExtraction-NLP
Web Scraping for Company Website Information

Objective

The goal of this project is to extract text content from the "About Us" or "Home" pages of various company websites. The extracted information will be saved in individual text files for further processing, such as keyword extraction or sentiment analysis.

Technologies Used:

Python for scripting

Pandas for handling company data from an Excel file

Requests for fetching webpage content

BeautifulSoup for parsing HTML

Selenium (optional) for handling dynamic websites

OS module for file handling

Project Workflow"

Read Company Data

The input is an Excel file  containing company names and their corresponding website URLs.

URLs are checked and formatted to ensure they include https:// if missing.

Web Scraping Process

Each company's website is accessed using the requests library.

If the website blocks automated requests, a Selenium-based approach can be used as a fallback.

The script extracts text from relevant HTML tags (<article>, <main>, <div class='content'>, <p>).

Titles are extracted from the <title> tag.

Data Storage

Extracted content is saved as a .txt file named after the company.

The files are stored in the Output directory.

Error Handling

Handles request failures (e.g., timeouts, blocked requests, missing pages).

If scraping fails, an error message is displayed for the company.

Challenges and Solutions:

Some websites block bots → Added browser-like headers to bypass simple bot detection.

Some pages are dynamically loaded → Selenium can be used for JavaScript-heavy pages.

Page structures vary across sites → The script attempts multiple HTML structures before defaulting to <p> tags.

Future Improvements

Implement NLP-based keyword extraction from the extracted text.

Store extracted content in a structured database instead of text files.

Automate detection of anti-bot mechanisms and switch to Selenium when needed.

This project is a fundamental step towards analyzing company information efficiently using web scraping and natural language processing.

