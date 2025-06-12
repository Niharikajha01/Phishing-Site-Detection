🛡️ ChatPhishDetector: Multi-Modal AI-Driven Phishing Detection
ChatPhishDetector is a robust and extensible phishing detection system that simulates real-world browsing behavior to uncover deceptive websites. Leveraging a combination of traditional web scraping, dynamic content rendering, image-based OCR, and large language models, it delivers advanced classification and phishing signal extraction.
🚀 Features
•	🌐 Static Crawling: Retrieves raw HTML using requests and BeautifulSoup for lightweight page analysis.
•	⚙️ Dynamic Rendering: Executes JavaScript-heavy content using Selenium with a headless Chrome browser.
•	🖼️ OCR & Image Analysis: Extracts and analyzes textual content from <img> elements using pytesseract.
•	📊 DOM Feature Extraction: Parses the DOM to extract forms, inputs, scripts, and structural cues.
•	🧠 Gemini LLM Integration: Synthesizes all extracted features and uses Gemini LLM to classify the site.
•	🔧 Modular Architecture: Organized for extensibility—add components like screenshots, alternate models, etc.
•	🔐 API Configurable: Keys managed securely in a settings.py configuration file.
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
│   └── dom_parser.py        # Extracts DOM components
├── analyzer/
│   ├── llm_formatter.py     # Builds prompt for Gemini
│   └── llm_analyzer.py      # Sends prompt to Gemini API
├── utils/
│   ├── logger.py            # Logging helper
│   └── helpers.py           # Utilities
├── data/
│   ├── screenshots/
│   ├── html_pages/
│   └── extracted_images/
└── outputs/
    └── results.json         # Final phishing classification

🛠️ Prerequisites
• Python 3.8+
• Google Chrome
• ChromeDriver (match browser version)
• Tesseract OCR engine installed and added to system PATH
📦 Installation
1. Clone the Repository:
   git clone https://github.com/yourusername/chatphishdetector.git
   cd chatphishdetector
2. Set Up Virtual Environment:
   python -m venv venv
   venv\Scripts\activate (Windows) or source venv/bin/activate (Unix)
3. Install Dependencies:
   pip install -r requirements.txt
4. Configure API Key:
   cp config/settings_example.py config/settings.py
   Paste your Gemini API key in settings.py
▶️ Usage
Run a phishing detection scan:
python main.py --url "https://example.com"
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
•	🔐 Cybersecurity automation
•	🧪 Academic research in phishing detection
•	🎓 Education and awareness platforms
•	🧠 Threat intelligence enrichment
🛣️ Roadmap
•	[x] Core multi-modal pipeline
•	[ ] Visual feature extraction via screenshots
•	[ ] Web UI dashboard
•	[ ] LLM alternatives: OpenAI, Claude, etc.
•	[ ] Browser extension for real-time analysis
🙌 Acknowledgments
•	BeautifulSoup - https://www.crummy.com/software/BeautifulSoup/
•	Selenium - https://www.selenium.dev/
•	Tesseract OCR - https://github.com/tesseract-ocr/tesseract
•	Google Gemini - https://deepmind.google/technologies/gemini/
📫 Contact
Niharika Jha
📧 niharikajha@example.com
🔗 GitHub: https://github.com/Niharikajha01
"Detection is no longer just about patterns—it's about perception and reasoning."
— ChatPhishDetector Team

