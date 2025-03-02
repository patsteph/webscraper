# WebScraper

A user-friendly Python tool for extracting and saving content from websites into document formats.

## 📋 Overview

WebScraper is a straightforward utility designed to help users extract relevant text content from web pages and save it in common document formats (DOCX, PDF). The tool removes unwanted elements like scripts, styling, code blocks, and excessive formatting to provide clean, readable content.

## ✨ Features

- **Clean Text Extraction**: Removes scripts, styles, code blocks, and other non-content elements
- **Smart Formatting**: Cleans up excessive whitespace and improves readability
- **Multiple Output Formats**: Save as Microsoft Word (DOCX) or PDF
- **User-Friendly Interface**: Simple command-line prompts guide you through the process
- **Custom Save Location**: Option to choose where to save your extracted content
- **Automatic Directory Creation**: Creates a "ScrapeOutputs" folder on your Desktop by default

## 🔧 Requirements

The script requires the following Python packages:

```
requests
beautifulsoup4
lxml
python-docx
reportlab
fake-useragent
```

## 📥 Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/webscraper.git
   cd webscraper
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

## 🚀 Usage

Run the script from your terminal or command prompt:

```
python webscraper.py
```

The script will guide you through the following steps:

1. Enter the URL of the website you want to scrape
2. Choose your preferred output format (DOCX or PDF)
3. Enter a name for the saved file
4. Decide whether to use the default save location or choose a custom one

## 🛠️ How It Works

1. **Fetching Content**: The script sends a request to the specified URL with a randomized user agent to avoid blocking
2. **Parsing and Cleaning**: BeautifulSoup extracts the relevant text content while removing unwanted elements
3. **Text Processing**: The extracted text is cleaned by removing excessive whitespace and formatting
4. **Saving**: The cleaned content is saved in your chosen format to either the default location or a custom directory

## 🧩 Function Descriptions

- `fetch_content(url)`: Retrieves the HTML content from the specified URL
- `clean_text(text)`: Removes excessive formatting and unwanted content
- `extract_text(html)`: Uses BeautifulSoup to extract relevant text from the HTML
- `get_output_directory()`: Creates and returns the path to the default output directory
- `sanitize_filename(filename)`: Ensures the filename is valid for all operating systems
- `save_as_docx(content, output_dir, filename)`: Saves the content as a Word document
- `save_as_pdf(content, output_dir, filename)`: Saves the content as a PDF document

## ⚠️ Limitations

- The script may not work properly on websites that use heavy JavaScript to load content
- Some websites may block web scraping attempts
- Very large pages may take longer to process or might be truncated in the output file
- PDF formatting is basic and doesn't preserve the original layout of the webpage

## 📜 Legal Considerations

Please be aware that web scraping may be subject to legal restrictions:

- Always check a website's Terms of Service before scraping
- Respect `robots.txt` files and scraping policies
- Do not overload websites with too many requests
- Only use the extracted content in accordance with copyright laws and fair use principles

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- [Requests](https://requests.readthedocs.io/) for HTTP requests
- [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/) for HTML parsing
- [python-docx](https://python-docx.readthedocs.io/) for DOCX file creation
- [ReportLab](https://www.reportlab.com/) for PDF generation
- [fake-useragent](https://pypi.org/project/fake-useragent/) for user agent rotation
