# Generalized Raw Text Data Scraper & Cleaner

A powerful, generalized Python tool designed for educational purposes to extract, clean, and structure raw HTML text data from any given URL (using IMDB as a primary benchmark) into well-organized CSV datasets.

## 📌 Project Overview
When scraping data from websites, standard text extraction often retrieves massive amounts of redundant data (such as page footers, navigation links, and generic site titles). This project introduces an algorithmic approach to solve the data-cleaning bottleneck. 

Instead of writing hardcoded custom rules for every single website, this tool implements a generalized sorting and frequency-based filtering logic to isolates useful data into primary columns while pushing non-essential data to the periphery.

> [!WARNING]
> **Educational Disclaimer:** This repository is strictly for educational, research, and academic purposes. Scraping web content may be subject to site-specific Terms of Service and robot.txt restrictions. The author assumes no liability for any misuse or policy violations. Use responsibly.

## 🧠 Algorithmic Framework & Workflow
The system processes web pages through a structured text-optimization pipeline:
1. **Dynamic HTML Retrieval:** Connects to the targeted URL (e.g., IMDB Movie Meter chart) and pulls down the complete HTML structural content.
2. **Redundant Class Filtering:** Identifies and strips out repetitive CSS classes and structural noise using optimized unique collection filtering (`set` operations).
3. **Text Node Extraction:** Loops through targeted class structures to extract internal inner text, systematically parsing out formatting breaks (`\n`), whitespace, and empty blocks.
4. **Data Sizing & Row Sorting:** Applies an elegant algorithmic logic that weights data nodes. By analyzing row counts and structural densities, the algorithm automatically moves high-value content blocks to the first columns while filtering out boilerplate layout text into trailing columns.
5. **Data Structuring & Export:** Transforms the final processed dictionary structures into a structured `pandas` DataFrame, executes transposition matrices (`df.transpose()`), and exports the final product into an organized, clean `.csv` file format ready for database seeding or analytical modeling.

## 🛠️ Technical Implementation
- **Language:** Python 3.x
- **Core Libraries:** BeautifulSoup (bs4), Pandas, Requests, Collections (OrderedDict).
- **Target Output:** Standardized, high-density `.csv` files completely filtered of web layout noises.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
