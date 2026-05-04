# test-automation-project
Singlish to Sinhala Transliteration - Test Automation
IT23583764 | IT3040 - ITPM | Assignment 1
Overview
This project tests the accuracy of the Chat Sinhala transliteration function available at pixelssuite.com/chat-translator.
It automates 50 negative test cases covering 24 Singlish input types using Playwright (Python).
---
Project Structure
```
test-automation-project/
│
├── test\_automation.py        # Main Playwright automation script
├── IT23583764\_Test cases.xlsx  # Test cases with results
└── README.md                 # This file
```
---
Prerequisites
Make sure the following are installed on your machine:
Python 3.8+ → https://www.python.org/downloads/
pip (comes with Python)
---
Installation
Step 1 - Clone the repository
```bash
git clone https://github.com/lccommit/test-automation-project.git
cd test-automation-project
```
Step 2 - Install required Python packages
```bash
pip install playwright openpyxl
```
Step 3 - Install Playwright browser
```bash
playwright install chromium
```
---
How to Run Tests
Make sure the Excel file is CLOSED before running.
```bash
python test\_automation.py --excel "IT23583764\_Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 8000 --type-delay-ms 100 --slow-mo-ms 300 --save-every 1 --keep-open
```
Command Parameters
Parameter	Value	Description
`--excel`	File path	Path to the Excel test cases file
`--url`	Website URL	The chat translator URL
`--wait-ms`	8000	Wait time (ms) for output to load
`--type-delay-ms`	100	Delay between keystrokes (ms)
`--slow-mo-ms`	300	Slow motion delay for browser actions
`--save-every`	1	Save Excel after every test case
`--keep-open`	-	Keep browser open after tests finish
---
Test Results
Results are automatically saved to the Excel file:
Column	Description
TC ID	Test case ID (Neg_0001 - Neg_0050)
Input length type	S (≤30), M (31-299), L (300-450) characters
Input	Singlish input text
Expected output	Correct Sinhala transliteration
Actual output	What the system actually outputs
Status	PASS / FAIL
Singlish input types covered	Input type category
Evidence or rationale	Reason for test case
---
Singlish Input Types Covered
#	Input Type
1	Question forms
2	Command forms
3	Greetings
4	Requests
5	Responses
6	Repeated Words
7	Inputs with Punctuation Marks
8	Romanization / Spelling Variants
9	Isolated English Word Insertions
10	Multi-Word English Phrases
11	English Digital Terms
12	Platform/App Names
13	English Abbreviations/Acronyms
14	English Clipped Forms
15	Place Names Embedded in Singlish
16	Person Names Embedded in Singlish
17	Inputs with Numbers and Numeric Suffixes
18	Inputs with Currency
19	Inputs with Time Formats
20	Inputs with Dates
21	Inputs with Unit of Measurements
22	Inputs with Slang and Casual Phrasing
23	Online Identifiers in Singlish
24	Inputs Containing Emojis
---
Tested Application
URL: https://www.pixelssuite.com/chat-translator
Function tested: Chat Sinhala transliteration only
Out of scope: Standard Sinhala, backend APIs, performance, security testing
---
Author
Student ID: IT23583764  
Module: IT3040 - IT Project Management  
Assignment: Assignment 1 - Option 1
