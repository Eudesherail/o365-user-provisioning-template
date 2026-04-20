# O365 User Provisioning Template

Structured Excel-based solution for standardized Office 365 account preparation and CSV-ready user provisioning workflows.

---

## Overview
This project demonstrates a structured approach to preparing Office 365 user account data using an Excel-based workflow.

It was designed to reduce manual effort, improve consistency, and minimize errors during bulk user provisioning processes.

---

## Problem
Manual user account creation in Office 365 environments can be inefficient and error-prone:

- inconsistent username formats  
- incorrect domain assignments  
- repetitive data entry  
- CSV formatting errors during import  

---

## Solution
This solution introduces a structured Excel-based workflow that:

- standardizes user input  
- enables controlled domain selection  
- generates consistent usernames automatically  
- prepares data in a CSV-compatible format  

---

## Workbook Structure

- **Edit**  
  Input sheet for user data (first name, last name, domain)

- **DomainList**  
  Centralized list of available domains for controlled selection

- **Result**  
  Automatically generated output formatted for Office 365 import

---

## Logic

The system generates usernames using a normalized format:

```text
firstname.lastname@domain
```

Additional processing includes:

- lowercase conversion  
- German umlaut normalization  
  - ä → ae  
  - ö → oe  
  - ü → ue  

### Example

```text
Jörg Müller → joerg.mueller@example.org
```

---

## Business Value

- reduces manual provisioning effort  
- minimizes human error  
- enforces naming consistency  
- supports scalable user creation workflows  

---

## Use Case

A user enters required account data into the input sheet.  
The system automatically generates standardized output, which can be exported as a CSV file and used directly for Office 365 bulk user import.

---

## Future Improvements

- integration with Power Automate for approval workflows  
- Power Apps interface for guided user input  
- SharePoint-based data source for domain management  
- direct user provisioning via Microsoft Graph API  

---

## Note

This project is based on a real-world internal workflow and has been abstracted for demonstration purposes.
