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
