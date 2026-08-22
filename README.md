# waygood-data-scraping-assignment
# Product Data Scraping & Cleaning Assignment

## Overview

This project was completed as part of the AI/ML & Data Scraping Intern technical assignment.

The objective was to collect publicly available university course information, clean and standardize the extracted data, and store it in structured JSON and CSV formats.

## Tools Used

* Python
* Requests
* BeautifulSoup
* Pandas
* JSON
* CSV

## Input

The assignment provided 10 publicly accessible university course URLs.

The URLs included courses from universities such as:

* University of Birmingham
* Heriot-Watt University
* University of Wollongong
* RIT Dubai
* Birmingham City University
* Solent University
* Queen's University Belfast
* University of Exeter
* London South Bank University
* University of Technology Sydney

## Workflow

```text
Course URLs
     ↓
Webpage Retrieval
     ↓
HTML Parsing
     ↓
Course Data Extraction
     ↓
Data Cleaning & Standardization
     ↓
Missing Value Handling
     ↓
JSON Dataset
     ↓
CSV Dataset
     ↓
Validation & Quality Checks
```

## Data Fields

The dataset contains the following fields:

* `universityName`
* `courseName`
* `courseLevel`
* `award`
* `duration`
* `durationInMonths`
* `campusName`
* `attendanceType`
* `deliveryFormat`
* `startDate`
* `firstYearTuitionFees`
* `applicationFeeAmount`
* `totalCreditHours`
* `entryRequirements`
* `careerOpportunities`
* `courseURL`
* `sourceUrl`
* `lastVerifiedDate`

## Data Cleaning

The extracted information was cleaned and standardized before being stored.

The cleaning process included:

* Removing irrelevant webpage content such as navigation and cookie-banner text.
* Standardizing extracted fields.
* Preserving the original course information where possible.
* Using `null` when information was not publicly available.
* Avoiding guessed or fabricated values.
* Checking for duplicate course URLs.
* Validating required fields and record counts.

## Handling Website Restrictions

Some university websites may use security mechanisms such as Cloudflare or AWS CloudFront that can prevent automated requests.

No CAPTCHA, login, or website security mechanism was bypassed.

Where automated extraction was not possible, information was manually verified using publicly accessible university webpages or official university documents/PDFs, in accordance with the assignment requirements.

## University of Exeter

The University of Exeter URL provided in the assignment points to an undergraduate degree directory rather than a specific course page.

A representative course from the publicly accessible directory was selected and structured according to the dataset schema.

## Validation

The final dataset was validated using Python.

The validation checks include:

* Valid JSON structure
* CSV readability
* Required columns
* Non-empty course and university names
* Course URL availability
* Duplicate URL detection
* Expected number of course records

Final dataset:

* **10 course records**
* **18 data fields**

## Output Files

### `extractor.py`

Python script used for data extraction, cleaning, and dataset generation.

### `courses.csv`

Final course-level dataset in CSV format.

### `courses.json`

Course-level dataset in JSON format.

### `university.json`

University-level dataset in JSON format.

### `tests/`

Contains test data and Python validation scripts used to verify the dataset.

### `answers.md`

Assignment-related answers and supporting information.

## How to Run

Install the required Python dependencies:

```bash
pip install -r requirements.txt
```

Run the extraction script:

```bash
python extractor.py
```

Run the validation tests:

```bash
python tests/test_validation.py
```

## Notes

All information was collected from publicly accessible sources. Missing information was represented as `null` rather than being inferred or fabricated.

The dataset was last verified on **18 August 2026**.
