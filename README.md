##Quality Management Document System

Power Apps, SharePoint, Power Automate

###Overview
This solution is a fully functional Quality Management Document System built on Microsoft Power Platform. It centralizes document creation, review, approval, versioning, and ongoing lifecycle management for Quality Assurance teams. The app is designed for controlled document environments where traceability, compliance, and audit readiness matter.

###Core Features
Document Management
Create, upload, and manage controlled documents
Metadata-driven categorization, no static folder dependencies
SharePoint as the primary data and file store
Automatic versioning, status tracking, and audit logs

Approvals and Workflow
Power Automate flows for review and sign-off
Multi-stage approval routing with timestamps
Automated notifications for pending tasks and expiring documents
Records and Lifecycle

Expiry monitoring with alerts
Activity tracking for view, edit, and approval events

“My Records” view for personalized document access

Role-based visibility for sensitive document sets
UI/UX
Fully responsive Power Apps canvas app
Collapsible metadata panels and dynamic filtering
Variable-based theme structure for quick branding changes
Integrated PDF preview support

###Architecture
Power Apps

Canvas application for document submission, review, metadata management, and search

Screens: Home, My Records, Approvals, Expiring Soon, Record Details, Dashboard

SharePoint

Primary storage for documents

Lists/Libraries:

Documents (Title, UploadDate, ExpiryDate, Status, Version, SubmittedBy, Approver, DocumentLink, Category metadata)

Approvers (role mapping)

Categories metadata (MainCategory, SubCategory, SubSubCategory)

Power Automate

Approval flow for document lifecycle

Expiry notification flow

Version control automation

Role-based access sync (optional)

Data Model

Documents List Fields

Title

DocumentLink

UploadDate

ExpiryDate

Status

Version

SubmittedBy

ApprovedBy

Category metadata (MainCategory, SubCategory, SubSubCategory)

Setup Instructions
Prerequisites

Power Apps license

SharePoint Online site

Power Automate license

Environment with Dataverse optional

Steps

Import the Power Apps solution file

Create the required SharePoint lists and libraries using the templates provided in /SharePointTemplates

Update data connections inside the Power App

Update the Power Automate flows with correct SharePoint URLs

Configure role mappings in the Approvers list

Publish the app and test all workflows

Deployment

Use the included Solution Package for ALM

Deploy through Power Platform Admin Center or manually import the solution zip

Store environment variables for site URLs, library names, and email groups

Governance and Security

Access is controlled through SharePoint permissions and role mapping

Finance or confidential categories can be restricted at library or item level

Logging and version history ensures audit readiness

Follow standard DLP policies to keep documents internal

Roadmap

AI-based auto-tagging for metadata

Enhanced PDF viewer with zoom and multi-page navigation

Analytics dashboard with Power BI integration

API endpoints for external system integration

Contact

For enhancements, issues, or feature requests, create an issue in this repository
