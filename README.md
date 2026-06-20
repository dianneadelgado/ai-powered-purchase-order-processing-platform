## Overview

An AI-powered document processing workflow built with n8n, Ollama, OCR, PostgreSQL, Google Drive, Gmail, and Google Sheets.

The system automatically monitors incoming documents, extracts structured information using OCR and a local LLM, validates the extracted data, notifies reviewers when issues are detected, and exports approved records into business systems.

---

## Business Problem

Many organizations still process purchase orders, invoices, forms, and other business documents manually.

This often leads to:

* Slow processing times
* Data entry errors
* Inconsistent records
* Increased operational costs
* Bottlenecks in approval workflows

---

## Solution

This platform automates the document processing lifecycle:

1. Detect new documents uploaded to Google Drive
2. Download and process files automatically
3. Extract text using OCR
4. Use a local LLM (Ollama Hermes) to identify key fields
5. Validate extracted information
6. Send Gmail notifications for exceptions or review requests
7. Generate document summaries
8. Export structured results to Google Sheets or ERP systems

---

## Workflow Architecture

```text
Google Drive Trigger
        │
        ▼
Download Document
        │
        ▼
OCR Extraction
        │
        ▼
Prepare OCR Text
        │
        ▼
AI Field Extraction (Ollama Hermes)
        │
        ▼
Validation Layer
        │
        ▼
 ┌─────────────┬─────────────┐
 │ Failed      │ Passed      │
 ▼             ▼
Gmail Alert    AI Summary
                     │
                     ▼
            Google Sheets Export
```

## Key Features

### Automated Document Intake

* Google Drive monitoring
* Automatic file processing
* Event-driven architecture

### OCR Processing

* Converts scanned documents into machine-readable text
* Supports PDF-based workflows

### AI Field Extraction

Extracts structured information such as:

* Purchase Order Number
* Vendor Name
* Invoice Number
* Dates
* Amounts
* Contact Information

### Data Validation

Validates extracted information before export.

Examples:

* Missing required fields
* Invalid formats
* Incomplete records

### Human Review Workflow

When validation fails:

* Gmail notification is generated
* Reviewer is alerted
* Manual verification can be performed

### Structured Data Export

Exports approved data to:

* Google Sheets
* ERP systems
* Databases
* Internal business tools

---

### AI

* Ollama
* Hermes LLM

### Data Storage

* PostgreSQL

### OCR

* OCR API Integration

### Notifications

* Gmail

### File Storage

* Google Drive

### Reporting

* Google Sheets

### Infrastructure

* Docker

---

## Example Use Cases

### Purchase Order Processing

Automatically extract:

* PO Number
* Supplier
* Amount
* Date

### Invoice Processing

Capture:

* Invoice Number
* Vendor Details
* Due Dates
* Payment Amounts

### Vendor Onboarding

Process submitted forms and extract company information.

### Contract Review

Extract key metadata and flag missing information for review.

---

## Benefits

* Reduced manual data entry
* Faster document processing
* Improved data quality
* Human-in-the-loop exception handling
* Scalable workflow architecture
* Local AI processing using Ollama

---

## Future Enhancements

* Confidence scoring
* Duplicate document detection
* ERP integrations
* Approval dashboard
* Analytics and reporting
* Multi-document classification

---

## Author

Dianne Delgado

An engineer focused on building AI-powered business automation systems that streamline operations and reduce manual work.

---

## Portfolio Project

This project demonstrates:

* Workflow Automation
* AI Integration
* OCR Processing
* Data Validation
* Business Process Automation
* Human-in-the-Loop Review Systems
* Docker-Based Deployment
* Local LLM Integration
