# Smart Identity Extractor & Cross-Document KYC Validator  
### IT594 – Final Project  
### Author: YOUR NAME  
### Roll No: YOUR ROLL  
---

## 📌 Project Overview  
This project automates the verification of identity documents used in digital KYC processes.  
Users typically upload documents such as:

- Aadhaar Card  
- PAN Card  
- Bank Statements / Cheques  

Along with a self-filled form containing personal details.

Manually checking all information for consistency is time-consuming and error-prone.  
This system performs:

✔ OCR extraction from all document images  
✔ Automatic field extraction (Name, DOB, PAN, Aadhaar, Account Number)  
✔ Normalization & cross-document comparison  
✔ KYC Consistency Scoring  
✔ JSON-based interpretable output  

All of this is done in **ONE Python file (`main.py`)**.

---

## 🧠 Features

### 🔹 1. OCR Engine  
- EasyOCR (CPU version)  
- Supports JPG, PNG, JPEG  
- Handles Aadhaar, PAN, Bank Docs  

### 🔹 2. Field Extraction Using Patterns  
Extracts:  
- Aadhaar Number (XXXX XXXX XXXX)  
- PAN Number (ABCDE1234F)  
- Date of Birth (DD/MM/YYYY)  
- Bank Account Number  
- Partial Name Detection  

### 🔹 3. KYC Score  
Compares extracted fields with user-provided form data (`sample_form_data.json`):

| Field | Weight |
|------|--------|
| Name | 0.30 |
| DOB | 0.15 |
| Aadhaar | 0.20 |
| PAN | 0.25 |
| Address | 0.10 |

Outputs a final score between **0–1**.

---

## 📁 Repository Structure

