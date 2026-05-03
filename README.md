# ITPM Assignment 1 - Transliteration Accuracy Testing

**Student Name:** SAMARANAYAKA P D D J  
**Registration Number:** IT23769670  
**Module:** IT3040 - Information Technology Project Management (ITPM)  
**Task:** Assignment 1 (Option 1) - Transliteration Accuracy Testing

---

## 📌 1. What is this Project?
This project is an automated software testing assignment designed to evaluate the transliteration accuracy of a live web application: [Chat Sinhala Translator](https://www.pixelssuite.com/chat-translator). 

The primary objective is to test how accurately the system converts informal, chat-style **Singlish** (Sinhala typed in English characters) into standard **Sinhala** text. The project aims to identify the weaknesses, boundary conditions, and algorithmic failures of the current transliteration engine using automated UI testing techniques.

## 🛠️ 2. What I Have Done
To thoroughly test the application's limits, I have successfully completed the following tasks as per the university guidelines:
* **Designed 50 Negative Test Cases:** Formulated exactly 50 test cases where the transliteration system completely fails to produce the expected Sinhala output.
* **Covered 24 Singlish Input Categories:** Ensured that all 24 specific Singlish typing behaviors are covered, with at least 2 test cases per category.
* **Length Constraints Analyzed:** Distributed the test cases across three string length constraints: Short (<=30 chars), Medium (31-299 chars), and Long (>=300 chars) to test the system's payload handling.
* **Documented Rationales:** Clearly documented the evidence and rationale for categorizing each test case.
* **Automated the Testing Process:** Used Playwright automation to programmatically feed these test cases into the web application and record the actual outputs/failures automatically.

## ⚙️ 3. How It Works (Technical Architecture)
This project utilizes **Python** and **Playwright** for end-to-end (E2E) UI test automation. 
1. **Data Ingestion:** The script reads the Singlish input data directly from the provided Excel file (`IT23769670.xlsx`).
2. **Automated Interaction:** Playwright launches a Chromium browser, navigates to the URL, and simulates human typing behavior.
3. **Data Extraction & Verification:** The script extracts the generated Sinhala output and compares it to the expected output.
4. **Reporting:** It automatically updates the "Actual Output" and "Status" (Pass/Fail/UI Error) back into the Excel spreadsheet.

---

## 🚀 4. Installation & Setup Instructions

To run this automation project locally, please follow these 5 steps carefully:

### Step 1: Install Prerequisites
* Install **Python 3.11 or 3.12** on your computer. *(Important: Make sure to check the "Add Python to PATH" box during installation).*
* Install **Google Chrome** (recommended) or allow Playwright to use its default Chromium browser.

### Step 2: Set Up the Project Environment
Clone this repository to your local machine using Git, or download it as a ZIP file and extract it (e.g., to your `D:` drive).
```bash
git clone [https://github.com/DilikaDilmith/ITPM-Assignment-1-NEW-TESTING.git](https://github.com/DilikaDilmith/ITPM-Assignment-1-NEW-TESTING.git)
cd ITPM-Assignment-1-NEW-TESTING
```
### Step 3: Open Terminal
Open your preferred terminal (Command Prompt, PowerShell, or the integrated terminal in VS Code) and ensure you are inside the extracted project folder.

### Step 4: Install Dependencies
Run the following commands in your terminal to install the required Python libraries and Playwright browsers:
```bash
pip install pandas openpyxl
pip install pytest-playwright
playwright install
```
### Step 5: Run the Automation Script
Once the setup is complete, execute the Python script by running the following command.
```bash
python test_automation.py --excel "IT23769670.xlsx" --url "[https://www.pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator)" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```
