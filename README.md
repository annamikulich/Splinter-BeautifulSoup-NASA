# 🪐 Mars Data Scraper – Splinter + BeautifulSoup

This project demonstrates automated web scraping of the latest Mars news and weather using Python tools like **Splinter**, **BeautifulSoup**, and **JSON**. All data is collected from publicly available NASA-related sources and compiled into a single JSON dataset.

---

## 🚀 Project Goals

- Scrape the latest Mars news title and teaser text  
- Extract current Mars weather data  
- Export the information as a structured `.json` file for future use

---

## 🗂 Project Structure

Mars_data/
├── part_1_mars_news.ipynb # Scrapes NASA Mars News site
├── part_2_mars_weather.ipynb # Scrapes Mars Weather updates
├── mars_data.json # Combined output in JSON format
└── README.md


---

## 💡 Technologies Used

- 🧠 `BeautifulSoup` – for parsing HTML content
- 🧪 `Splinter` – browser automation (headless Chrome)
- 🔧 `json` – for structured data output
- 🌐 Websites scraped:
  - https://redplanetscience.com
  - https://mars.nasa.gov

---

## 📦 Dependencies

To install all required libraries:

```bash
pip install splinter beautifulsoup4 selenium webdriver-manager
⚙️ Example Workflow

🔹 News Scraping
from bs4 import BeautifulSoup
from splinter import Browser

browser = Browser('chrome')
browser.visit("https://redplanetscience.com")
html = browser.html
soup = BeautifulSoup(html, 'html.parser')

news_title = soup.find("div", class_="content_title").text
news_p = soup.find("div", class_="article_teaser_body").text
🔹 Output JSON
{
  "news_title": "NASA Discovers New Clues to Mars Water History",
  "news_paragraph": "Researchers have discovered ancient lakebeds...",
  "weather": "Sol 4122 (2025-05-27): Sunny, -68°C / -82°C"
}
📁 Output

The resulting data is saved in:

mars_data.json
It can later be used for dashboards, reports, or as input for machine learning pipelines.

📌 Use Cases

Teaching web scraping and automation
Creating Mars-themed dashboards
Daily ETL ingestion of planetary data
Backend enrichment for space apps
