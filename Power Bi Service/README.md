🟦 1. Introduction to Power BI Service

Power BI Service is a cloud-based SaaS platform used to publish, share, collaborate, and manage Power BI reports and dashboards.

🔹 Ecosystem

Power BI Desktop → Report development
Power BI Service → Sharing & governance
Power BI Mobile → Consumption

🔹 Licensing

Free → Personal use
Pro → Collaboration & sharing
Premium → Enterprise capacity & advanced features

🟦 2. Workspaces & Collaboration

Workspaces are collaborative environments in Power BI Service where reports, semantic models (datasets), dashboards, and dataflows are stored and managed.

They are used to control access, organize content, and manage development lifecycle.

🔹 Types of Workspaces
1️⃣ My Workspace

Personal workspace
Used for individual development
Not recommended for enterprise collaboration

2️⃣ New (V2) Workspaces

Used for team collaboration
Supports role-based access
Required for App publishing
Supports deployment pipelines (Premium)

🔹 Workspace Roles

Power BI Service provides four main roles:

🔸 Admin
Full control over workspace
Add/remove users
Publish, delete, manage content
Update App

🔸 Member
Can publish, edit, and delete content
Cannot manage workspace settings (unless allowed)

🔸 Contributor
Can create and modify content
Cannot publish/update App
Cannot manage workspace access

🔸 Viewer
Read-only access
Can view reports and dashboards
Cannot edit or publish

🔹 Best Practices for Workspaces

✔ Separate Dev / Test / Production workspaces
✔ Avoid using My Workspace for production content
✔ Limit Admin access
✔ Assign dataset ownership clearly
✔ Use Apps for business user distribution

🔹 Workspace vs App

Workspace → For developers and collaborators
App → For business users (read-only consumption)

🔹 Enterprise Usage Scenario

In a real organization:

Developers build reports in Dev workspace
Tested reports move to Test workspace
Final approved reports move to Production workspace
Production content is distributed via App

This ensures governance and controlled deployment.

🟦 3. Datasets (Semantic Models) & Refresh

A Semantic Model (Dataset) is the data model published from Power BI Desktop to Power BI Service.
It contains tables, relationships, measures, calculated columns, and business logic.

Reports connect to semantic models for visualization.

🔹 Dataset vs Report

Dataset (Semantic Model) → Data + Model + Measures

Report → Visual layer built on top of dataset

Multiple reports can use the same dataset.

🔹 Data Refresh

Power BI Service supports:

🔸 On-Demand Refresh

Manual refresh triggered by user.

🔸 Scheduled Refresh

Automatic refresh at defined intervals (daily, multiple times per day).

🔸 Incremental Refresh

Only refreshes new/changed data instead of full dataset (improves performance).

🔹 Gateway

Required when data source is on-premises.

Types:

Personal Gateway → Single user

Standard Gateway → Enterprise-level shared gateway

🔹 Best Practices

✔ Use scheduled refresh for production datasets
✔ Monitor refresh history regularly
✔ Use incremental refresh for large datasets
✔ Separate dataset workspace from report workspace (enterprise design)

🟦 4. Sharing & Distribution

Power BI Service allows secure report distribution across users.

🔹 Sharing Reports

Reports can be shared:

Directly with specific users

Through workspace access

Through published Apps

Users need Pro license (or Premium capacity).

🔹 Apps

Apps are packaged collections of:

Reports

Dashboards

Datasets

Apps are:

Read-only for business users

Used for enterprise distribution

Updated centrally by workspace Admin

🔹 Row-Level Security (RLS)

RLS restricts data visibility based on user role.

Process:

Define roles in Desktop

Publish to Service

Assign users to roles

Example:

Sales manager sees only their region

HR sees only HR department data

🔹 Best Practices

✔ Use Apps for production distribution
✔ Avoid direct sharing in large organizations
✔ Always test RLS before deployment

🟦 5. Dashboards & Monitoring

Dashboards are created in Power BI Service and combine visuals from one or multiple reports.

🔹 Dashboards

Created only in Service

Pin visuals from reports

Combine multiple datasets

Used for executive summary view

🔹 Alerts

Alerts can be set on KPI tiles to notify users when:

Value crosses threshold

Metric increases/decreases

🔹 Subscriptions

Users can subscribe to:

Reports

Dashboards

Emails are sent at scheduled intervals.

🔹 Usage Metrics

Power BI provides built-in usage reports:

Number of views

Active users

Report popularity

Used to track adoption.

🟦 6. Governance & Security

Governance ensures controlled, secure, and compliant BI deployment.

🔹 Admin Portal

Used by tenant administrators to manage:

Sharing policies

Export permissions

Publish to web restrictions

Dataset usage controls

🔹 Lineage View

Shows relationships between:

Data sources

Dataflows

Datasets

Reports

Dashboards

Helps in impact analysis.

🔹 Endorsement

Datasets can be:

Promoted → Recommended dataset

Certified → Official trusted dataset

Used to maintain data quality standards.

🔹 Sensitivity Labels

Used for data classification:

Confidential

Internal

Public

Supports compliance and data protection.

🟦 7. Advanced Features

These features are mostly available in Premium or advanced environments.

🔹 Deployment Pipelines

Used for lifecycle management:

Dev → Test → Production

Allows comparison and controlled deployment.

🔹 Dataflows

Cloud-based data transformation using Power Query in Service.

Benefits:

Reusable transformations

Centralized data preparation

Supports enterprise modeling

🔹 Paginated Reports

Pixel-perfect reports designed for:

Printing

Regulatory reporting

Invoice-style outputs

Built using Power BI Report Builder.

🔹 Large Dataset Storage

Premium feature allowing:

Larger model sizes

Better performance handling
