# Spain-keywords-analysis
This project automatically scrapes SEO-related content from any given blog/article URL, extracts keywords using NLP techniques, analyzes their trends using Google Trends (PyTrends), and generates a detailed Excel report with Tail-Type categorization (Short-Tail, Mid-Tail, Long-Tail).

📌 Features
✅ Web Scraping

Extracts Title, Meta Description, H1-H3 Tags, Body Content, Blog Tags, and Internal Links from any URL.

✅ Keyword Extraction (NLP)

Uses RAKE (Rapid Automatic Keyword Extraction) & NLTK to extract relevant SEO keywords.

Cleans text by removing stopwords, duplicates, and punctuation.

Categorizes keywords into:

Short-tail (2 words)

Mid-tail (3 words)

Long-tail (4+ words)

✅ Keyword Trend Analysis

Uses PyTrends (Google Trends Python API) to get search volume (average over time).

Difficulty & CPC are placeholders (can be extended with Google Ads API).

✅ Automated Report Generation

Exports results into Excel (Keyword_Analysis_Report.xlsx) with columns:

mathematica
Copy
Edit
Keyword | Source URL | Volume | Difficulty | CPC | Tail-Type
📂 Project Structure
bash
Copy
Edit
📁 keyword-analysis-automation
 ├── keyword_scraper.py            # Main Python script
 ├── Keyword_Analysis_Report.xlsx   # Auto-generated report
 ├── requirements.txt               # Python dependencies
 └── README.md                      # Project documentation
⚙️ Installation & Setup
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/keyword-analysis-automation.git
cd keyword-analysis-automation
2. Install Dependencies
Create requirements.txt with:

nginx
Copy
Edit
requests
beautifulsoup4
lxml
pandas
nltk
rake-nltk
pytrends
openpyxl
Install them:

bash
Copy
Edit
pip install -r requirements.txt
Download NLTK stopwords:

python
Copy
Edit
import nltk
nltk.download('stopwords')
🚀 Running the Script
Run the script with:

bash
Copy
Edit
python keyword_scraper.py
The script will:

Ask you for a URL

Scrape and extract keywords

Analyze keyword volumes via Google Trends

Generate an Excel report automatically

✅ After execution, you’ll get:
Keyword_Analysis_Report.xlsx – SEO-ready keyword list with volume and Tail-Type.

📊 Sample Output (Excel)
Keyword	Source URL	Volume	Difficulty	CPC	Tail-Type
travel tips spain	https://sample.com/article	78	N/A	N/A	Mid Tail
best places visit	https://sample.com/article	102	N/A	N/A	Long Tail
spanish tapas	https://sample.com/article	65	N/A	N/A	Short Tail

🔧 To-Do / Future Improvements
✅ Integrate Google Ads API for real CPC & Keyword Difficulty

✅ Push reports to Google Sheets automatically

✅ Auto-email / Slack Notification with daily/weekly reports

🤝 Contributing
Pull requests and suggestions are welcome!
