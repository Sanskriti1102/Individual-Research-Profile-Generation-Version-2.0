# 🧠 Individual-Research-Profile-Generation (Version 2.0)

🧾 **Based on:** [Original Version 1.0 by Sanskriti1102](https://github.com/Sanskriti1102/Individual-Research-Profile-Generation)

---

🔰 **Introduction**

**Individual-Research-Profile-Generation v2.0** is a modern, browser-based academic scraping tool that automates the extraction of Google Scholar publications using Selenium and a user-provided scholar list.

> No code. No command line. Just upload, enter, click — and download your professor's full research list instantly.

---

🌟 **Why This Matters**

Academic data is spread, scattered, and painful to retrieve — especially across multiple authors. This tool:

✅ Empowers students, researchers, assistants, and institutions to collect profiles in minutes  
✅ Converts Google Scholar profiles to clean Excel reports  
✅ Works even on free-tier cloud services like Streamlit Cloud  

---

📥 **Input**

Upload an Excel file with the following format:

| Name           | Scholar ID     | 
|----------------|----------------|
| John Doe       | abcDefGhIjK    | 
| Jane Smith     | qRsTuVwXyZ     | 

- Scholar ID is the `user=` part from a Google Scholar profile URL  
- You can add any number of rows

✏️ Enter the professor name into the input field  
📤 Click **Scrape Publications**

---

📤 **Output**

An Excel file containing all scraped publication details, structured as:

| Title                              | Authors               | Publication Date | Document Type | Link                                           |
|-----------------------------------|-----------------------|------------------|---------------|------------------------------------------------|
| Deep Learning in Biomedicine      | John Doe, Alice Y.    | 2024             | Other         | https://scholar.google.com/some-paper-link     |

You can download this file instantly from the app.

---

🧠 **Tech Stack**

🖥️ **Frontend:** Streamlit  
🕷️ **Scraping Engine:** Selenium WebDriver with headless Chromium  
📊 **Data Handling:** OpenPyXL (Excel), Pandas  
📦 **Runtime:** Python 3.x  

---

🛠️ **How It Works**

1. Loads the input Excel and extracts the Scholar ID of the professor  
2. Opens their Google Scholar profile in headless Chrome  
3. Scrolls and clicks "Show more" until all publications are loaded  
4. Scrapes title, author, date, and link for each publication  
5. Saves the result into a downloadable Excel file  

---

🧪 **Setup for Local Usage**

```bash
git clone https://github.com/yourusername/Individual-Research-Profile-Generation-Version-2.0.git
cd Individual-Research-Profile-Generation-Version-2.0

pip install -r requirements.txt

streamlit run Scrapper.py
📦 requirements.txt

streamlit
selenium
openpyxl

🔧 apt-packages.txt

chromium-chromedriver
chromium-browser

🧠 Chrome is invoked headlessly using:

options.binary_location = '/usr/bin/chromium-browser'
self.driver = Chrome(executable_path='/usr/bin/chromedriver', options=options)

📈 Current Limitations

⚠️ Requires scholar IDs to be present in the uploaded Excel
⚠️ Only supports public Google Scholar profiles
⚠️ Scrapes metadata (no full-text or citation graphs)

🚀 Future Roadmap

🔍 Keyword filtering and smart search inside profiles
📄 PDF + citation export options
📊 Cross-professor comparison dashboard
🤖 Integrate with Semantic Scholar API for citation metrics
📱 Mobile-friendly Streamlit layout
🛰️ Batch processing mode for lab groups or institutions

🎓 Project Legacy

Originally developed as a CLI tool in Version 1.0
Now reborn with a no-code UI in Version 2.0, built by Intelligenz Talks

🧵 Empowering researchers one click at a time.

📬 For suggestions, bugs, or feature requests — open an issue or drop a DM on LinkedIn.

If you want the ZIP pack with this plus `requirements.txt` and `apt-packages.txt`, just say the word. Otherwise, this baby is ready to be your repo’s crown jewel. 👑

Lemme know!
