# Quality Management Document System  
Built with Microsoft Power Apps, SharePoint, and Power Automate

## Overview  
This repository contains a complete Quality Management Document System designed for controlled document environments where compliance, traceability, and audit readiness are non-negotiable. The solution manages the full document lifecycle from creation to approval and expiry.

## Core Features  

### Document Management  
- Upload and manage controlled documents  
- Metadata-driven categorization  
- Built-in versioning and document status tracking  
- SharePoint as secure document storage  

### Workflow and Approvals  
- Multi-stage approval via Power Automate  
- Timestamped review history  
- Automated notifications and reminders  
- Routing based on roles or categories  

### Lifecycle and Records  
- Expiry tracking and proactive alerts  
- Activity auditing: viewed, edited, approved  
- “My Records” personalized view  
- Role-based visibility for sensitive documents  

### UI and User Experience  
- Fully responsive Canvas App  
- Collapsible metadata panels  
- Dynamic filtering and searching  
- Variable-based theming for quick branding updates  
- PDF preview integration  

## Architecture  

### Power Apps  
Canvas application containing:  
- **Home**  
- **My Records**  
- **Record Details**  
- **Approvals**  
- **Expiring Soon**  
- **Dashboard**

### SharePoint (Data Layer)  
Libraries and lists used:  
- **Documents Library**  
  - Title  
  - DocumentLink  
  - UploadDate  
  - ExpiryDate  
  - Status  
  - Version  
  - SubmittedBy  
  - ApprovedBy  
  - Category metadata: MainCategory, SubCategory, SubSubCategory  
- **Approvers List**  
- **Metadata List** (for cascading categories)

### Power Automate  
- Document approval workflow  
- Expiring document alert workflow  
- Versioning automation flow  
- Optional access-control synchronization

## Installation and Setup  

### Prerequisites  
- Power Apps license  
- SharePoint Online site  
- Power Automate license  
- Power Platform environment

### Steps  
1. Import the solution package from this repository.  
2. Create the necessary SharePoint lists and libraries using the provided templates (if included).  
3. Open the Power App and update all data connections.  
4. Configure all Power Automate flows with the correct SharePoint URLs.  
5. Populate the **Approvers** list with roles and email mappings.  
6. Publish the application and test the entire document lifecycle.

## Deployment  
- Deploy via Power Platform Admin Center or Solution Import.  
- Configure environment variables for site URLs, library names, and email groups.  
- Follow recommended ALM procedures for packaging and release management.

## Governance and Security  
- Document access controlled via SharePoint permissions.  
- Role-based restrictions for Finance or sensitive categories.  
- Full logging and version history ensures audit readiness.  
- Complies with enterprise DLP policies.

## Roadmap  
- AI-driven metadata auto-tagging  
- Enhanced PDF viewer with zoom and navigation  
- Power BI dashboards for document analytics  
- External API integration endpoints

## Support  
Submit issues, bugs, or enhancement requests through GitHub Issues.

