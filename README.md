# REAL-WORLD-FINANCIAL-CONSUMER-COMPLAINTS-TABLEAU-DASHBOARD-VISUALIZATION
Tableau Financial Complaints dashboard is based on Real World Fake Data #RWFD which is helpful in creating real life dashboards.

📊 Project Overview
An interactive Tableau dashboard analyzing financial consumer complaints data from the Real World Fake Data (RWFD) dataset. This comprehensive visualization provides insights into complaint patterns, resolution rates, geographic distribution, and company responsiveness across various financial products and services.
🎯 Objective
The primary objective of this dashboard is to:

Analyze and visualize consumer complaint trends across different financial products and services
Track company response effectiveness and resolution metrics
Identify geographic patterns in complaint distribution
Monitor complaint resolution timelines and dispute rates
Provide actionable insights for financial institutions and regulatory bodies
Enable data-driven decision making through interactive filtering and drill-down capabilities

📝 Description
This dashboard leverages the RWFD dataset containing 75,513 complaint records spanning from December 2011 to October 2020. The visualization is built using Tableau's advanced features including:

Interactive hex map visualization for geographic distribution
Dynamic filtering with 7 interactive parameters
Multi-dimensional analysis across products, issues, submission channels, and company responses
KPI tracking with visual gauges and trend indicators
Detailed drill-down capabilities through tooltips and detail tables

Data Sources

Primary Dataset: Financial Consumer Complaints.csv
Geographic Mapping: Hex Map (Excel file for state abbreviations and coordinates)
Data Join: Left join on State field to enable hex map visualization

🔑 Key Performance Indicators (KPIs)
The dashboard tracks four critical KPIs with visual gauge indicators:
1. Timely Response Rate

Percentage of complaints receiving timely responses from companies
Indicates company compliance with response time requirements
Visual gauge showing performance against benchmarks

2. In Progress Rate

Percentage of complaints currently being processed
Tracks active complaint volume and processing efficiency
Helps identify potential backlog situations

3. Disputed Rate

Percentage of complaints disputed by consumers after resolution
Indicates consumer satisfaction with resolution outcomes
Key metric for quality of complaint handling

4. Resolved at No Cost Rate

Percentage of complaints closed without monetary relief to consumers
Tracks non-monetary resolution effectiveness
Important for understanding resolution strategies

📈 Dashboard Components
Main Visualizations

Complaints by Location (Hex Map)

Interactive hex tile map showing complaint distribution across U.S. states
Color-coded intensity showing complaint volume
Clickable states for detailed filtering
Includes state abbreviations for easy identification


Complaints by Product (Horizontal Bar Chart)

Top financial products by complaint volume:

Credit card or prepaid card
Mortgage
Debt collection
Bank account or service
Checking or savings account
Credit card
Student loan
Vehicle loan or lease


Interactive tooltips showing sub-product breakdown


Complaints by Issue (Horizontal Bar Chart)

Most common complaint issues sorted by frequency
Detailed sub-issue information in tooltips
Enables quick identification of problem areas


Complaint Resolution Trends (Stacked Bar Chart)

Time-series visualization of company responses
Categories include:

Closed
Closed with explanation
Closed with monetary relief
Closed with non-monetary relief
In progress
Untimely response


Shows resolution pattern evolution over time


Submission Channel Analysis (Bar Chart)

Breakdown of complaint submission methods:

Web
Referral
Phone
Postal mail
Fax
Email


Helps understand customer preferred communication channels


Consumer Dispute Analysis (Pie Chart)

Visual representation of disputed vs. non-disputed complaints
Quick metric for overall customer satisfaction


Detail Table

Comprehensive record-level view
Sortable and filterable columns
Includes all key complaint attributes



🎛️ Interactive Filters
The dashboard includes seven dynamic parameter controls:

Select Year

Range: 2011 - 2020
Enables year-over-year comparison
Default: 2011


Select State

All U.S. states including territories
Default: All States
Synchronized with hex map selection


Start Date

Custom date range filtering (beginning)
Default: December 1, 2011


End Date

Custom date range filtering (end)
Default: October 13, 2020


Company Response

Filter by response type:

All Responses
Closed
Closed with explanation
Closed with monetary relief
Closed with non-monetary relief
Closed without relief
In progress
Untimely response




Product

Filter by financial product type
Includes all product categories
Default: All Products


Issue

Filter by specific complaint issues
70+ issue categories available
Default: All Issues



📊 Data Fields
Core Attributes

Complaint ID: Unique identifier for each complaint
Date Submitted: When the complaint was filed
Date Received: When the company received the complaint
Product: Type of financial product
Sub-product: Specific product subcategory
Issue: Primary complaint issue
Sub-issue: Detailed issue description
Company: Name of the financial institution
State: U.S. state of the complainant
ZIP Code: Geographic identifier
Tags: Additional categorization (e.g., Older American, Servicemember)
Consumer Consent Provided: Whether consumer agreed to share complaint
Submitted Via: Channel used to submit complaint
Company Response to Consumer: Resolution type
Timely Response?: Boolean indicator
Consumer Disputed?: Whether consumer disputed the resolution
Company Public Response: Public statement from company

Calculated Fields

Total Complaints: COUNTD([Complaint ID])
State Highlight: [State]=[Parameters].[Parameter 2]
Date Range Filter: [Date Submitted] >= [Start Date] AND [Date Submitted] <= [End Date]
Rounded Column: ROUND([Column], 0) for hex map positioning
Gauge Metrics: MIN(0) and MIN(1) for KPI gauge visualization

🛠️ Technical Details
Tableau Version

Built with: Tableau Desktop 2021.1.0
Compatibility: Tableau Desktop 2021.1 and later
Format: Tableau Packaged Workbook (.twbx)

Data Extract

Records: 75,513 complaints
Refresh Date: July 24, 2021
Storage: Hyper extract for optimal performance
Encoding: UTF-8

Design Features

Responsive layout optimized for desktop viewing
Color-coded visualizations following Tableau best practices
Tooltips enhanced with Viz in Tooltip for sub-categories
Custom shapes and images for visual appeal
Professional color palette for clarity and accessibility

🎨 Visual Design Principles

Color Scheme: Professional blues and grays for business intelligence
Layout: Logical flow from overview (KPIs) to details
Interactivity: Intuitive click-and-filter functionality
Typography: Clear, readable fonts with appropriate sizing
White Space: Balanced use of space for visual clarity

💡 Key Insights & Use Cases
For Regulatory Bodies

Monitor industry-wide complaint trends
Identify problematic products or practices
Track company compliance with response requirements
Geographic hotspot analysis

For Financial Institutions

Benchmark against industry standards
Identify operational improvement areas
Track resolution effectiveness
Understand customer pain points

For Consumer Advocates

Understand common consumer issues
Track resolution fairness and effectiveness
Identify patterns requiring policy intervention

For Data Analysts

Demonstrate advanced Tableau capabilities
Showcase interactive dashboard design
Example of effective data storytelling
Portfolio project for data visualization skills

📁 Repository Structure
├── Financial_Complaints_Dashboard____RWFD.twbx    # Main Tableau workbook
├── README.md                                       # This file
├── screenshots/                                    # Dashboard screenshots
├── data/                                          # Sample data files (if included)
└── documentation/                                 # Additional documentation
