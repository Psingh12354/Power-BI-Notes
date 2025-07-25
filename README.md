

# Power-BI-Notes

## What is Power BI?

**Microsoft Power BI** is a business intelligence and data visualization platform designed to help organizations and professionals analyze, visualize, and share insights from their data. Power BI caters to users ranging from business analysts to data scientists, offering interactive dashboards and a variety of visualizations such as graphs, maps, charts, and scatter plots. The tool also features **AI Insights**, harnessing artificial intelligence and machine learning algorithms to uncover patterns, trends, and actionable insights within datasets.

**Key Capabilities:**

- Interactive and customizable dashboards.
- Advanced data modeling and DAX (Data Analysis Expressions) calculations.
- Seamless integration with numerous data sources (cloud services, databases, web APIs, spreadsheets, etc.).
- Collaboration features through the Power BI Service (cloud), enabling reports and dashboards to be shared with teams and embedded in other apps.
- Data refresh scheduling and automatic updates.


## Excel vs Power BI

**Main Differences:**


| Criteria | Excel | Power BI |
| :-- | :-- | :-- |
| **Primary Use** | Data organization, calculations | Business intelligence, data visualization |
| **Data Handling Capacity** | Limited (up to ~1M rows/sheet) | Large/Big Data sets (Multi-million rows) |
| **Connectivity** | Basic (files, some databases) | Extensive (cloud, on-prem, APIs, services) |
| **Visualizations/Dashboards** | Basic, static, less interactive | Rich, interactive and dynamic |
| **Processing Speed** | Slower with large data | Optimized engine, faster processing |
| **User Experience** | Familiar for many users, but can limit | Modern, user-friendly, designed for BI |
| **Collaboration/Mobile** | Limited sharing; no app | Real-time cloud collaboration; mobile apps |
| **AI \& Automation** | Minimal (basic formulas/macros) | Built-in AI insights, natural language Q\&A |

**Summary of Differences:**

- Power BI is tailored for better data visualization, analytics, and sharing large-scale business intelligence reports, while Excel excels in organizing and transforming small to medium data, and running ad-hoc analysis.
- Power BI's connectivity to diverse data sources and advanced interactivity significantly surpasses that of Excel.
- Power BI dashboards are interactive, visually rich, and can be effortlessly shared or embedded across platforms, including mobile devices.


## Power BI Architecture

Power BI Service's architecture is typically divided into:

- **Front End Cluster**: This is the interface layer interacting with users and clients. In this layer, most of the data modeling, visualizations, and user queries take place. It delivers dashboards and reports to users.
- **Back End Cluster**: This layer manages data processing, dataflows, security, and storage. The **Power Query Editor** runs here, performing ETL (Extract, Transform, Load) operations on source data before it is visualized. Other services in the back end handle authentication, data refresh, and collaboration features.

**Note:** Power BI Desktop (the desktop authoring tool) also uses a local version of the Power Query Editor for ETL and modeling before publishing to the Power BI Service.

## Database Normalization

**Database normalization** is a systematic process used in relational database design to organize data in such a way that redundancy is minimized and data integrity is improved. The primary objective is to structure tables so that each represents a single topic, with relationships between topics managed via keys.

**Goals of Normalization:**

- **Eliminate redundant data** (e.g., storing the same data in more than one table).
- **Ensure data dependencies make sense** (data is logically stored).
- Improve consistency, reduce update anomalies.
- Facilitate easier maintenance and scalability.

**Normal Forms:**
Normalization is carried out in stages called "normal forms." Common forms include:


| Normal Form | Description |
| :-- | :-- |
| **1st Normal Form (1NF)** | Remove duplicate columns; ensure each cell contains atomic values. |
| **2nd Normal Form (2NF)** | Meet 1NF and move data subsets that apply to multiple rows to separate tables; establish relationships using foreign keys. |
| **3rd Normal Form (3NF)** | Meet 2NF and remove columns not dependent on the primary key. |
| **BCNF** | Stricter version of 3NF, handles special dependency cases. |

**Example:**
An unnormalized sales table storing customer, product, and sales info (including repeated customer addresses) would be split into separate tables for Customers, Products, and Sales. The result is less repetition, more consistent updates, and easier scaling.

**Benefits of Normalization:**

- Reduces data redundancy and improves storage efficiency.
- Enhances data integrity and accuracy.
- Makes data easier to query and maintain.

**Potential Limitation:**
Sometimes, over-normalization can make querying more complex, as data will be spread across more tables, often requiring multiple joins. In analytical models (e.g., Power BI), a balance is often struck between normalized structure and query/report performance.

---
