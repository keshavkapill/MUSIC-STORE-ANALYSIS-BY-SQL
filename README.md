<div align="center">

# 🎵 MUSIC STORE ANALYSIS

### <i>Turning Music Store Data Into Business Insights</i>

<p>
<strong>SQL • PostgreSQL • Data Analytics • Relational Database • Business Intelligence</strong>
</p>

<a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL">
<img src="https://img.shields.io/badge/📂%20VIEW%20REPOSITORY-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>
<a href="https://www.linkedin.com/in/keshavkapil15/">
<img src="https://img.shields.io/badge/💼%20LINKEDIN-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,35:312E81,70:6D28D9,100:00C2FF&height=250&section=header&text=🎵%20Music%20Store%20Analysis&fontSize=45&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Turning%20Music%20Store%20Data%20Into%20Business%20Insights&descAlignY=63&descSize=17"/>

</div>

---

<div align="center">

### 🎯 `DATA → DATABASE → SQL → ANALYSIS → INSIGHTS`

<img src="https://img.shields.io/badge/SQL-Data%20Analytics-336791?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/pgAdmin4-Database%20Management-336791?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Data%20Analytics-Business%20Insights-8A2BE2?style=for-the-badge"/>

<br>

<img src="https://img.shields.io/badge/JOINS-SQL-FF8C00?style=for-the-badge"/>
<img src="https://img.shields.io/badge/SUBQUERIES-SQL-8A2BE2?style=for-the-badge"/>
<img src="https://img.shields.io/badge/CTEs-SQL-007ACC?style=for-the-badge"/>
<img src="https://img.shields.io/badge/WINDOW%20FUNCTIONS-SQL-E53935?style=for-the-badge"/>

</div>

---

# 🎧 PROJECT OVERVIEW

> **Music Store Analysis** is an end-to-end SQL Data Analytics project designed to transform a relational music-store database into meaningful business insights.

The project works with interconnected information related to:

**Customers • Invoices • Invoice Items • Tracks • Albums • Artists • Genres • Playlists • Employees**

Instead of simply retrieving database records, the project focuses on answering practical analytical questions involving:

* 👥 Customer purchasing behaviour
* 💰 Revenue and sales performance
* 🎵 Music and genre preferences
* 🎸 Artist and track analysis
* 🌍 Geographic purchasing patterns
* 🏆 Customer spending
* 📊 Business-oriented decision making

The complete workflow moves from **understanding the database** to **asking business questions**, then using SQL to extract and interpret the required information.

---

# 🧭 PROJECT FLOW

```text
                    🎵 MUSIC STORE DATA
                            │
                            ▼
                  🗂️ DATASET / CSV FILES
                            │
                            ▼
                  🗄️ RELATIONAL DATABASE
                            │
                            ▼
                  🔍 BUSINESS QUESTIONS
                            │
                            ▼
                    💻 SQL ANALYSIS
                            │
             ┌──────────────┼──────────────┐
             ▼              ▼              ▼
        👥 CUSTOMER      💰 SALES       🎵 MUSIC
        ANALYSIS        ANALYSIS       ANALYSIS
             │              │              │
             └──────────────┼──────────────┘
                            ▼
                     🌍 GEO ANALYSIS
                            │
                            ▼
                    📊 FINAL INSIGHTS
                            │
             ┌──────────────┴──────────────┐
             ▼                             ▼
       📄 ANALYSIS REPORT             📊 PRESENTATION
```

---

# 🔴 01 — PROBLEM STATEMENT

A digital music store generates large amounts of transactional and catalogue data.

However, storing data is not the same as understanding it.

The database contains information about:

```text
Customers
    ↓
Invoices
    ↓
Invoice Lines
    ↓
Tracks
    ↓
Albums
    ↓
Artists
    ↓
Genres
```

The challenge is to connect these different entities and answer questions such as:

> **Who are the highest-value customers?**

> **Which countries generate the most revenue?**

> **Which genres are most popular?**

> **Which artists have the largest catalogue?**

> **Which customer spends the most within each country?**

> **How can SQL transform transactional records into useful business information?**

This project addresses these questions through structured relational SQL analysis.

---

# 🟢 02 — PROJECT OBJECTIVE

The primary objective is to demonstrate how **SQL can be used as a complete analytical tool** for extracting business insights from a relational database.

### Key objectives

```text
✓ Understand the relational database structure

✓ Explore customer and transaction data

✓ Analyse revenue and purchasing behaviour

✓ Identify high-value customers

✓ Analyse genres, artists and tracks

✓ Study country-level purchasing patterns

✓ Use advanced SQL techniques

✓ Convert query results into business insights
```

---

# 🔵 03 — ANALYTICAL APPROACH

The project follows a progressive analytical workflow.

### LEVEL 01 — DATA UNDERSTANDING

Understand the available entities, attributes and relationships.

### LEVEL 02 — DATA EXPLORATION

Explore records using filtering, sorting and aggregation.

### LEVEL 03 — RELATIONAL ANALYSIS

Connect multiple tables using appropriate joins.

### LEVEL 04 — BUSINESS ANALYSIS

Convert business questions into SQL queries.

### LEVEL 05 — ADVANCED SQL

Use:

```text
JOINs
Subqueries
CTEs
Window Functions
Aggregate Functions
GROUP BY
HAVING
ORDER BY
CASE
```

### LEVEL 06 — INSIGHT GENERATION

Interpret query results from a business perspective rather than stopping at raw output.

---

# 🗄️ DATABASE ARCHITECTURE

The project is based on a relational music-store database.

```text
                         🎵 MUSIC STORE DATABASE
                                  │
             ┌────────────────────┼────────────────────┐
             │                    │                    │
             ▼                    ▼                    ▼
        👥 CUSTOMER           🧾 INVOICE            👨‍💼 EMPLOYEE
             │                    │
             │                    ▼
             │              📋 INVOICE LINE
             │                    │
             │                    ▼
             │                 🎵 TRACK
             │                    │
             │              ┌─────┴─────┐
             │              ▼           ▼
             │          💿 ALBUM      🎼 GENRE
             │              │
             │              ▼
             │           🎤 ARTIST
             │
             └───────────────┐
                             ▼
                        🎧 PLAYLIST
                             │
                             ▼
                      🔗 PLAYLIST TRACK
```

---

# 🔗 RELATIONSHIP LOGIC

The database becomes analytically powerful because its tables are connected through relationships.

```text
CUSTOMER
   │
   │ customer_id
   ▼
INVOICE
   │
   │ invoice_id
   ▼
INVOICE_LINE
   │
   │ track_id
   ▼
TRACK
   │
   ├──────────────► ALBUM
   │                    │
   │                    ▼
   │                  ARTIST
   │
   └──────────────► GENRE
```

This structure allows a query to travel across multiple entities.

For example:

```text
Customer
   ↓
Invoice
   ↓
Invoice Line
   ↓
Track
   ↓
Genre
```

This makes it possible to investigate questions such as:

**Which genres generate the highest purchasing activity?**

---

# 🖼️ DATABASE SCHEMA

The repository contains the database schema/ER representation used to understand the relationships between the entities.

The schema is important because it provides the structural foundation for the SQL analysis.

### Core analytical entities

| Entity          | Analytical Purpose                            |
| --------------- | --------------------------------------------- |
| 👥 Customer     | Customer information and purchasing behaviour |
| 🧾 Invoice      | Transaction-level sales information           |
| 📋 Invoice Line | Individual purchased items                    |
| 🎵 Track        | Individual music tracks                       |
| 💿 Album        | Album-level information                       |
| 🎤 Artist       | Artist-level analysis                         |
| 🎼 Genre        | Music-category analysis                       |
| 🎧 Playlist     | Playlist information                          |
| 👨‍💼 Employee  | Employee/support information                  |

---

# 🎯 BUSINESS QUESTIONS

The project is organized around business-oriented questions rather than isolated SQL syntax.

## 👥 CUSTOMER ANALYSIS

Questions include:

* Who is the highest-spending customer?
* Which customers contribute the most revenue?
* How much does each customer spend?
* Who is the highest-spending customer within each country?
* How does purchasing behaviour vary across customers?

---

## 💰 SALES & REVENUE ANALYSIS

The project investigates:

* Revenue generated across countries
* Customer purchasing activity
* Invoice-level sales
* Revenue contribution by customers
* Geographic purchasing patterns
* Sales distribution

---

## 🎵 MUSIC ANALYSIS

The database can be used to investigate:

* Most popular genres
* Artists with the largest number of tracks
* Track-level purchasing behaviour
* Album relationships
* Music catalogue characteristics
* Customer music preferences

---

## 🌍 GEOGRAPHIC ANALYSIS

Geographic analysis connects customer location with purchasing behaviour.

Examples include:

```text
Country
   ↓
Customers
   ↓
Invoices
   ↓
Revenue
   ↓
Music Preferences
```

This enables questions such as:

* Which countries generate the most revenue?
* Which genre is most popular within a country?
* Who is the highest-spending customer in each country?

---

# 🧠 SQL CONCEPTS USED

## 01 — BASIC QUERYING

```sql
SELECT
FROM
WHERE
ORDER BY
GROUP BY
DISTINCT
LIMIT
```

These concepts are used for initial data exploration and filtering.

---

## 02 — AGGREGATE FUNCTIONS

```sql
COUNT()
SUM()
AVG()
MIN()
MAX()
```

Example:

```sql
SELECT
    country,
    SUM(total) AS revenue
FROM invoice
GROUP BY country;
```

This converts individual transactions into country-level business metrics.

---

## 03 — JOINS

Joins form the backbone of the relational analysis.

Example:

```sql
SELECT
    c.first_name,
    c.last_name,
    i.total
FROM customer c
JOIN invoice i
    ON c.customer_id = i.customer_id;
```

The query connects customer information with invoice transactions.

---

## 04 — MULTI-TABLE JOINS

More complex questions require multiple relationships.

```text
CUSTOMER
    ↓
INVOICE
    ↓
INVOICE_LINE
    ↓
TRACK
    ↓
ALBUM
    ↓
ARTIST / GENRE
```

This allows customer transactions to be connected with music metadata.

---

## 05 — SUBQUERIES

Subqueries allow one query to become part of another analytical calculation.

```text
MAIN QUERY
     │
     ▼
SUBQUERY
     │
     ▼
CALCULATED RESULT
     │
     ▼
FINAL ANALYSIS
```

They are particularly useful when comparing individual results against calculated values.

---

## 06 — COMMON TABLE EXPRESSIONS

CTEs improve the readability and organization of complex analytical queries.

Example:

```sql
WITH customer_sales AS
(
    SELECT
        customer_id,
        SUM(total) AS total_spent
    FROM invoice
    GROUP BY customer_id
)

SELECT *
FROM customer_sales;
```

This creates an intermediate analytical result that can be reused by the main query.

---

## 07 — WINDOW FUNCTIONS

Advanced analytical questions can be solved using window functions such as:

```sql
ROW_NUMBER()
RANK()
DENSE_RANK()
SUM() OVER()
AVG() OVER()
```

These are particularly useful for ranking customers and performing group-level comparisons.

---

# 🧩 ANALYTICAL CATEGORIES

<div align="center">

|    👥 CUSTOMER   |       💰 SALES       | 🎵 MUSIC |      🌍 GEOGRAPHY      |
| :--------------: | :------------------: | :------: | :--------------------: |
|     Spending     |        Revenue       |  Genres  |        Countries       |
|     Purchases    |       Invoices       |  Artists |  Customer Distribution |
|     Customers    |    Sales Activity    |  Tracks  |     Regional Demand    |
| Customer Ranking | Revenue Contribution |  Albums  | Country-level Spending |

</div>

---

# 🔄 END-TO-END ANALYTICS PIPELINE

```text
┌───────────────────────────┐
│       RAW DATA            │
│      CSV / SQL DATA       │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│   DATABASE UNDERSTANDING  │
│   Tables + Relationships  │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│    BUSINESS QUESTIONS     │
│ What do we want to know?  │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│       SQL QUERIES         │
│ JOIN + GROUP + FILTER     │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│     ANALYTICAL OUTPUT     │
│ Rankings + Aggregations   │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│     BUSINESS INSIGHTS     │
│ Data → Information        │
└───────────────────────────┘
```

---

# 🛠️ TECHNOLOGY STACK

<div align="center">

<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/pgAdmin4-336791?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Data%20Analytics-8A2BE2?style=for-the-badge"/>

</div>

| Technology            | Purpose                                 |
| --------------------- | --------------------------------------- |
| 🐘 **PostgreSQL**     | Relational database management          |
| 💻 **SQL**            | Data querying and analytical processing |
| 🖥️ **pgAdmin 4**     | Database management and query execution |
| 📊 **Data Analytics** | Business-question-driven analysis       |
| 📁 **CSV**            | Dataset resources                       |

---

# 📁 REPOSITORY STRUCTURE

The repository is organized around the complete analytics workflow.

```text
MUSIC-STORE-ANALYSIS-BY-SQL/
│
├── 📁 DataAnalyst-Question/
│   └── Business / analytical questions
│
├── 📁 DataSet_CSV/
│   └── CSV dataset resources
│
├── 📁 SQL-File-DataSet/
│   └── SQL / database resources
│
├── 📄 Music_Store-DataAnalysis-Report.pdf
│
├── 📊 Music_Store-DataAnalysis-Report.pptx
│
└── 📘 README.md
```

---

# 📋 PROJECT RESOURCES

### 📌 DATA ANALYST QUESTIONS

The `DataAnalyst-Question` directory contains the analytical questions that define the problems being investigated.

**Purpose:**

```text
Business Question
       ↓
SQL Problem
       ↓
Query
       ↓
Result
       ↓
Insight
```

---

### 🗃️ DATASET

The `DataSet_CSV` directory contains the CSV-based dataset resources used within the project.

The dataset represents the different entities required to recreate and analyse the music-store database.

---

### 💻 SQL DATABASE FILES

The `SQL-File-DataSet` directory contains the SQL/database resources used for working with the project.

These resources provide the foundation for:

* Database creation
* Data loading
* Table structure
* SQL analysis
* Query execution

---

### 📄 DATA ANALYSIS REPORT

The repository includes:

**`Music_Store-DataAnalysis-Report.pdf`**

The report provides a consolidated presentation of the analytical work and project findings.

---

### 📊 PROJECT PRESENTATION

The repository also includes:

**`Music_Store-DataAnalysis-Report.pptx`**

This presentation provides a visual summary of the project and its analytical outcomes.

---

# 🚀 HOW TO RUN / EXPLORE THE PROJECT

## STEP 01 — Install PostgreSQL

Install PostgreSQL and ensure that PostgreSQL is running correctly.

---

## STEP 02 — Open pgAdmin 4

Launch pgAdmin 4 and connect to your PostgreSQL server.

---

## STEP 03 — Create / Load the Database

Use the SQL resources available inside:

```text
SQL-File-DataSet/
```

to create and populate the required database.

---

## STEP 04 — Understand the Schema

Before running analytical queries, inspect the relationships between:

```text
Customer
Invoice
Invoice Line
Track
Album
Artist
Genre
Playlist
Employee
```

Understanding these relationships is essential for writing correct joins.

---

## STEP 05 — Review the Questions

Open:

```text
DataAnalyst-Question/
```

and identify the business question you want to investigate.

---

## STEP 06 — Write / Execute SQL

Use PostgreSQL / pgAdmin 4 to execute the relevant SQL analysis.

---

## STEP 07 — Interpret the Results

Do not stop at obtaining a table of results.

The final stage is:

```text
QUERY RESULT
     ↓
PATTERN
     ↓
OBSERVATION
     ↓
BUSINESS MEANING
```

---

# 📊 WHAT THIS PROJECT DEMONSTRATES

This project demonstrates practical understanding of:

```text
✓ Relational Database Concepts
✓ SQL Querying
✓ Data Exploration
✓ Data Aggregation
✓ Multi-table JOINs
✓ Subqueries
✓ CTEs
✓ Window Functions
✓ Customer Analytics
✓ Revenue Analysis
✓ Geographic Analysis
✓ Music Catalogue Analysis
✓ Business Question Formulation
✓ Data-driven Insight Generation
```

---

# 💼 REAL-WORLD APPLICATION

The same analytical approach can be applied to many real-world business domains.

```text
🎵 Music Store
      │
      ├── Customer Analytics
      ├── Revenue Analytics
      ├── Product Analytics
      ├── Geographic Analytics
      └── Behavioural Analytics
```

The same methodology can be transferred to:

* E-commerce
* Retail
* Subscription businesses
* Streaming platforms
* Banking
* SaaS products
* Marketing analytics
* Customer relationship management

The domain changes, but the analytical process remains similar:

> **Understand → Query → Analyse → Interpret → Decide**

---

# 🧠 KEY LEARNING OUTCOMES

Through this project, the following concepts can be practiced in a realistic context:

### DATABASE THINKING

Understanding how real-world entities are represented through relational tables.

### SQL THINKING

Converting a business question into a structured SQL query.

### RELATIONAL THINKING

Understanding how different entities connect through primary and foreign keys.

### ANALYTICAL THINKING

Moving beyond raw numbers and identifying meaningful patterns.

### BUSINESS THINKING

Understanding why a particular result matters rather than simply producing the result.

---

# 📈 PROJECT MATURITY

```text
LEVEL 01
DATA COLLECTION
     ↓
LEVEL 02
DATABASE STRUCTURE
     ↓
LEVEL 03
SQL EXPLORATION
     ↓
LEVEL 04
RELATIONAL ANALYSIS
     ↓
LEVEL 05
ADVANCED SQL
     ↓
LEVEL 06
BUSINESS INSIGHTS
```

This makes the project more than a collection of SQL queries.

It represents a complete **SQL-based analytical workflow**.

---

# 🔮 FUTURE ENHANCEMENTS

Potential extensions to the project include:

* 📊 Build an interactive Power BI dashboard
* 📈 Add visual sales and customer KPIs
* 🌍 Create geographic revenue visualizations
* 👥 Develop customer segmentation
* 🎵 Analyse genre-level customer preferences
* 📅 Add time-series revenue analysis
* 🏆 Create customer ranking dashboards
* 🔄 Automate the SQL-to-dashboard pipeline
* 📌 Add advanced business KPIs

---

# 📚 PROJECT DOCUMENTATION

<div align="center">

<a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/tree/main/DataAnalyst-Question">
<img src="https://img.shields.io/badge/📋%20DATA%20ANALYST%20QUESTIONS-FF6B35?style=for-the-badge"/>
</a>

<a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/tree/main/DataSet_CSV">
<img src="https://img.shields.io/badge/🗃️%20DATASET-00A86B?style=for-the-badge"/>
</a>

<a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/tree/main/SQL-File-DataSet">
<img src="https://img.shields.io/badge/💻%20SQL%20FILES-4169E1?style=for-the-badge"/>
</a>

<br><br>

<a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/blob/main/Music_Store-DataAnalysis-Report.pdf">
<img src="https://img.shields.io/badge/📄%20ANALYSIS%20REPORT-E53935?style=for-the-badge"/>
</a>

<a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/blob/main/Music_Store-DataAnalysis-Report.pptx">
<img src="https://img.shields.io/badge/📊%20PROJECT%20PRESENTATION-8A2BE2?style=for-the-badge"/>
</a>

</div>

---

# 👨‍💻 AUTHOR

<div align="center">

<img src="https://img.shields.io/badge/KESHAV%20KAPIL-Data%20Analytics%20%7C%20SQL%20%7C%20Cloud-7C3AED?style=for-the-badge"/>

### BTech Computer Science Engineering

**SQL • Data Analytics • Cloud • Full-Stack Development**

<br>

<a href="https://github.com/keshavkapill">
<img src="https://img.shields.io/badge/GitHub-KESHAVKAPILL-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="https://www.linkedin.com/in/keshavkapil15/">
<img src="https://img.shields.io/badge/LinkedIn-KESHAVKAPIL15-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

</div>

---

<div align="center">

### 🎵 `TURNING DATA INTO INSIGHTS — ONE QUERY AT A TIME`

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00C2FF,35:6D28D9,70:312E81,100:0F172A&height=120&section=footer"/>

**Made with ❤️ by Keshav Kapil**

</div>
