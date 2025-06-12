🛡️ ChatPhishDetector: Multi-Modal AI-Driven Phishing Detection

ChatPhishDetector is a robust and extensible phishing detection system that simulates real-world browsing behavior to uncover deceptive websites. Leveraging a combination of traditional web scraping, dynamic content rendering, image-based OCR, and large language models, it delivers advanced classification and phishing signal extraction.

🚀 Features

🌐 Static Crawling: Retrieves raw HTML using requests and BeautifulSoup for lightweight page analysis.

⚙️ Dynamic Rendering: Executes JavaScript-heavy content using Selenium with a headless Chrome browser to mimic real user browsing.

🖼️ OCR & Image Analysis: Extracts and analyzes textual content from <img> elements using pytesseract and image downloaders.

📊 DOM Feature Extraction: Parses the DOM to extract forms, inputs, scripts, and structural cues commonly found in phishing websites.

🧠 Gemini LLM Integration: Synthesizes all extracted features into a prompt and uses Google's Gemini LLM to classify the site as phishing or legitimate.

🔧 Modular Architecture: Highly organized, making it easy to add new components like screenshots, alternate models, or UI layers.

🔐 API Configurable: API keys and environment variables are securely managed via a settings.py configuration file.

🗂️ Folder Structure

chatphishdetector/
├── main.py                  # Entry point for running the full pipeline
├── requirements.txt         # Python dependencies
├── config/
│   └── settings_example.py  # Template config file (rename to settings.py)
├── crawler/
│   ├── static_crawler.py    # Fetches raw HTML
│   └── dynamic_crawler.py   # Loads JavaScript using Selenium
├── extractor/
│   ├── image_extractor.py   # Downloads image resources
│   ├── ocr.py               # Runs Tesseract OCR
│   └── dom_parser.py        # Extracts DOM components like forms and scripts
├── analyzer/
│   ├── llm_formatter.py     # Builds prompt for Gemini
│   └── llm_analyzer.py      # Sends prompt to Gemini API and receives verdict
├── utils/
│   ├── logger.py            # Logging helper
│   └── helpers.py           # Utilities for path management and normalization
├── data/
│   ├── screenshots/         # (Optional) Full-page website screenshots
│   ├── html_pages/          # Stored raw HTML
│   └── extracted_images/    # Image assets used for OCR
└── outputs/
    └── results.json         # Final phishing classification and details

🛠️ Prerequisites

Python 3.8+

Google Chrome (latest)

ChromeDriver (matching your Chrome version)

Tesseract OCR installed and in your system PATH

📦 Installation

Clone the Repository:

git clone https://github.com/yourusername/chatphishdetector.git
cd chatphishdetector

Set Up Virtual Environment:

python -m venv venv
-On Windows:
venv\Scripts\activate
-On Unix/MacOS:
source venv/bin/activate

Install Dependencies:

pip install -r requirements.txt

Configure API Key:

cp config/settings_example.py config/settings.py
-Open settings.py and paste your Gemini API key

▶️ Usage

Run a phishing detection scan:

python main.py --url "https://example.com"

The following steps will occur:

Static and dynamic crawling

Image download + OCR

DOM element parsing

Gemini LLM prompt creation and analysis

Output written to outputs/results.json

📌 Example Output (outputs/results.json)

{
  "url": "https://example.com",
  "verdict": "phishing",
  "confidence": 0.92,
  "analysis": {
    "forms": 3,
    "scripts": 6,
    "ocr_text": "Login Now to Secure Account",
    "llm_reasoning": "Detected common phishing phrases and suspicious form placements."
  }
}

📚 Use Cases

🔐 Cybersecurity automation

🧪 Academic research in phishing detection

🎓 Education and awareness platforms

🧠 Threat intelligence enrichment

🛣️ Roadmap



🙌 Acknowledgments

BeautifulSoup

Selenium

Tesseract OCR

Google Gemini

📫 Contact

Niharika Jha📧 jhaniharika983@gmail.com🔗 GitHub: github.com/Niharikajha01

"Detection is no longer just about patterns—it's about perception and reasoning."

