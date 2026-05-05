# Playwright Test Automation for Chat Translator

This repository contains the test automation project for the Chat Translator system (Singlish to Sinhala).

## Project Structure
- [IT23740310_test_automation.py](IT23740310/IT23740310_test_automation.py): The main Python script using Playwright for browser automation.
- `IT23740310 - Assignment 1 - Test cases.xlsx`: Excel file containing the test cases and results (Ensure this file is placed in the project directory).

## Setup Instructions

### 1. Prerequisites
Ensure you have Python 3.8+ installed on your system.

### 2. Install Dependencies
Run the following commands in your terminal:
```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

### 3. Run the Tests
Open PowerShell and navigate to the project folder:
```powershell
cd /path/to/project
```

Then execute the automation script:
```powershell
python IT23740310_test_automation.py --excel "IT23740310 - Assignment 1 - Test cases.xlsx" --sheet " Test cases" --header-row 1 --input-col "Input" --expected-col "Expected output" --actual-col "Actual output" --status-col "Status" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 10000 --retry-wait-ms 1500 --retries 10 --type-delay-ms 80 --slow-mo-ms 300 --save-every 1 --keep-open
```

## Configuration Parameters
- `--excel`: Path to the Excel file containing test cases.
- `--sheet`: Excel sheet name.
- `--header-row`: Header row number.
- `--input-col`: Excel column containing the Singlish input text.
- `--expected-col`: Excel column containing the expected Sinhala output.
- `--actual-col`: Excel column where the actual result is saved.
- `--status-col`: Excel column where PASS or FAIL is saved.
- `--url`: The website URL to test.
- `--wait-ms`: Initial wait time for the translation to appear.
- `--retry-wait-ms`: Time to wait between retries if output hasn't updated.
- `--retries`: Number of times to check for an output update.
- `--type-delay-ms`: Delay between typing each character.
- `--slow-mo-ms`: Slows down Playwright operations.
- `--save-every`: Saves the workbook after every N rows.
- `--keep-open`: Keeps the browser open after the run.

## Common Errors

### Python cannot open the script file
Ensure you are running the command from the `IT23740310` subfolder:
```powershell
cd D:\test_automation-IT23740310\IT23740310
```

### Excel file not found
Check if the Excel file exists at the specified path and the filename matches exactly.
