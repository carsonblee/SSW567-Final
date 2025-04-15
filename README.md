# SSW567 Final Project: Group F
Check Digit Calculation: Adler 32 algorithm

## Specifications
### Specification #1: Scanning the MRZ of a Travel Document
The system shall define an empty method to interface with a hardware device scanner, which provides two standardized MRZ strings (line 1 and line 2) directly in ICAO-compliant format. Preprocessing tasks such as OCR tuning or image enhancement are assumed to be handled by the hardware device.

### Specification #2: Decoding MRZ Strings into Fields and Identifying Check Digits
The system shall decode the two ICAO-compliant MRZ strings into their respective fields (e.g., document type, issuing country, name, passport number, etc.) and extract check digits for validation. Non-standard or incomplete MRZ inputs shall trigger an error message specifying the issue.

### Specification #3: Encoding Information Fields into MRZ Strings
The system shall encode travel document information fields into two ICAO-compliant MRZ strings following strict formatting rules (e.g., transliteration of special characters, YYMMDD date format). Missing database fields shall halt encoding and generate an error message.

### Specification #4: Reporting Mismatches Between Fields and Check Digits
The system shall validate each field against its respective check digit during processing. Any mismatch shall be reported immediately with a detailed error message specifying the field name, expected check digit, calculated check digit, and discrepancy type. Reports shall follow a standardized format for consistency.
