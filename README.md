# 🎵 Music Store Analysis
### SQL Data Analytics • Relational Database • Business Insights

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:141E30,50:243B55,100:00A8C6&height=270&section=header&text=🎵%20Music%20Store%20Analysis&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Turning%20Music%20Store%20Data%20Into%20Business%20Insights&descAlignY=65&descSize=17"/>
</p>

<p align="center">

<strong>
A practical SQL Data Analytics project that explores customers, sales,
music preferences, revenue and geographical performance using a relational database.
</strong>

</p>

<p align="center">

<a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL">
<img src="https://img.shields.io/badge/📂%20Repository-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="https://www.linkedin.com/in/keshavkapil15/">
<img src="https://img.shields.io/badge/💼%20LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

</p>

<p align="center">

<img src="https://img.shields.io/badge/SQL-Data%20Analytics-336791?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/pgAdmin4-Database%20Management-336791?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Data%20Analytics-Business%20Insights-00A86B?style=for-the-badge"/>

</p>

<p align="center">

<img src="https://img.shields.io/badge/JOINS-Advanced-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/SUBQUERIES-SQL-purple?style=for-the-badge"/>
<img src="https://img.shields.io/badge/CTEs-SQL-blue?style=for-the-badge"/>
<img src="https://img.shields.io/badge/WINDOW%20FUNCTIONS-SQL-red?style=for-the-badge"/>

</p>

---

# 🎧 Project Overview

**Music Store Analysis** is an end-to-end **SQL Data Analytics project** built around a relational music-store database.

The purpose of this project is to take raw transactional data and answer meaningful business questions using SQL.

Instead of simply writing queries, the project follows a complete analytical process:

> **Understand the data → Ask business questions → Query the database → Analyze the results → Extract insights**

<br>

<!-- ===================================================== -->
<!-- 🔴 PROBLEM STATEMENT -->
<!-- ===================================================== -->

<table>
<tr>
<td style="border: 2px solid #ff1744; padding: 24px; background-color: #120b0e;">

<h2 style="color:#ff1744;">
🔴 01 — PROBLEM STATEMENT
</h2>

<hr style="border: 0; border-top: 1px solid #ff1744;">

A digital music store generates data across multiple interconnected entities including **customers, invoices, tracks, albums, artists, genres, employees, and playlists**.

The challenge is to convert this relational data into meaningful business information that can answer questions around **customer purchasing behaviour, sales performance, music preferences, artist popularity, and geographic demand**.

This project addresses the problem through structured SQL analysis, transforming raw database records into insights that can support data-driven understanding of the music-store business.

</td>
</tr>
</table>

<br>

<!-- ===================================================== -->
<!-- 🟢 APPROACH -->
<!-- ===================================================== -->

<table>
<tr>
<td style="border: 2px solid #00e676; padding: 24px; background-color: #07130d;">

<h2 style="color:#00e676;">
🟢 02 — APPROACH
</h2>

<hr style="border: 0; border-top: 1px solid #00e676;">

The project follows an **end-to-end SQL data analysis workflow**.

The database is explored using fundamental and advanced SQL concepts including **SELECT, filtering, JOINs, GROUP BY, ORDER BY, aggregate functions, subqueries, and nested queries**.

The analysis begins with general business questions such as invoice activity, customer spending, revenue by location, and employee information. It then progresses into deeper analysis of **artists, genres, tracks, customer preferences, and geographic purchasing behaviour**.

Advanced queries combine multiple relational tables to determine patterns such as **genre popularity by country** and **the highest-spending customer within each country**.

</td>
</tr>
</table>

<br>

<!-- ===================================================== -->
<!-- 🔵 FINDINGS -->
<!-- ===================================================== -->

<table>
<tr>
<td style="border: 2px solid #00e5ff; padding: 24px; background-color: #061216;">

<h2 style="color:#00e5ff;">
🔵 03 — FINDINGS
</h2>

<hr style="border: 0; border-top: 1px solid #00e5ff;">

The SQL analysis reveals meaningful patterns across the music-store database.

The project identifies **high-value customers, leading artists, popular genres, purchasing activity across countries, and customer spending behaviour**. It also analyses tracks based on characteristics such as duration and examines customer interactions with specific music genres.

The advanced analysis provides a geographic perspective by identifying the **most popular genre in individual countries** and the **highest-spending customer in each country**.

Overall, the project demonstrates how SQL can connect multiple relational tables and transform transactional and catalogue data into structured **business intelligence and actionable analytical insights**.

</td>
</tr>
</table>

---

# 💡 What Does This Project Actually Do?

Imagine a music store with thousands of customers, invoices, tracks, albums and artists.

The database contains a lot of information, but raw data alone does not answer questions such as:

> 🎯 Who spends the most?

> 🌍 Which country generates the highest revenue?

> 🎵 What music genre is most popular?

> 🎸 Which artists have the most Rock tracks?

> 👥 Which customers are the most valuable?

This project uses **SQL as the analytical tool** to turn those questions into measurable answers.

---

# 🗄️ Database Schema

The project is built around a relational **Music Store Database** containing interconnected entities such as:

- 👤 **Customer**
- 🧾 **Invoice**
- 📋 **Invoice Line**
- 🎵 **Track**
- 💿 **Album**
- 🎤 **Artist**
- 🎼 **Genre**
- 👨‍💼 **Employee**
- 🎧 **Playlist**
- 🔗 **Playlist Track**
- 🌍 **Country / Location**

The relationships between these tables allow SQL queries to connect customer activity, purchases, tracks, albums, artists and genres.

### Music Store Database Schema

<p align="center">

<img 
src="https://user-images.githubusercontent.com/112153548/213707717-bfc9f479-52d9-407b-99e1-e94db7ae10a3.png"
alt="Music Store Database Schema"
width="850"
/>

</p>

---

# 🔄 Complete Analytical Flow

The complete analytical process can be represented as:

```text
                 🎵 RAW MUSIC STORE DATA
                          │
                          ▼
                   🗄️ RELATIONAL DB
                          │
                          ▼
                    🔍 EXPLORE DATA
                          │
                          ▼
                 ❓ BUSINESS QUESTIONS
                          │
                          ▼
                     💻 SQL
                          │
              ┌───────────┼───────────┐
              │           │           │
              ▼           ▼           ▼
          👥 CUSTOMER   💰 SALES    🎵 MUSIC
           ANALYSIS    ANALYSIS    ANALYSIS
              │           │           │
              └───────────┼───────────┘
                          │
                          ▼
                    📊 INSIGHTS
                          │
                          ▼
                    💡 DECISIONS
