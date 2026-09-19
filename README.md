<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🎵 Music Store Analysis - SQL Data Analytics</title>
  <style>
    :root {
      --bg-color: #0d1117;
      --card-bg: #161b22;
      --border-color: #30363d;
      --text-main: #c9d1d9;
      --text-heading: #ffffff;
      --accent-cyan: #00e5ff;
      --accent-blue: #4169e1;
      --accent-purple: #8a2be2;
      --accent-red: #ff1744;
      --accent-green: #00e676;
      --code-bg: #1f242c;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: var(--bg-color);
      color: var(--text-main);
      line-height: 1.6;
      padding: 20px;
    }

    .container {
      max-width: 1000px;
      margin: 0 auto;
    }

    /* Header & Banners */
    .header-banner {
      width: 100%;
      border-radius: 8px;
      overflow: hidden;
      margin-bottom: 20px;
    }

    .header-banner img {
      width: 100%;
      display: block;
    }

    .subtitle {
      text-align: center;
      font-size: 1.25rem;
      font-weight: 600;
      color: var(--text-heading);
      margin-bottom: 20px;
    }

    /* Centered Button & Badge Groups */
    .badge-group {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-bottom: 20px;
    }

    .badge-group img {
      height: 28px;
    }

    hr {
      border: 0;
      height: 1px;
      background: var(--border-color);
      margin: 30px 0;
    }

    /* Section Styling */
    h2 {
      font-size: 1.75rem;
      color: var(--text-heading);
      margin-bottom: 15px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    h3 {
      font-size: 1.25rem;
      color: var(--text-heading);
      margin: 15px 0 10px 0;
    }

    p {
      margin-bottom: 15px;
    }

    ul {
      margin-left: 20px;
      margin-bottom: 15px;
    }

    li {
      margin-bottom: 6px;
    }

    /* ASCII Diagrams & Code Blocks */
    .ascii-diagram, code-block {
      background-color: var(--code-bg);
      border: 1px solid var(--border-color);
      border-radius: 6px;
      padding: 15px;
      font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, Courier, monospace;
      font-size: 0.88rem;
      color: #e6edf3;
      overflow-x: auto;
      white-space: pre;
      margin-bottom: 20px;
    }

    pre code {
      background-color: transparent;
      padding: 0;
    }

    /* Problem Statement, Approach & Findings Cards */
    .card-section {
      display: flex;
      flex-direction: column;
      gap: 20px;
      margin-bottom: 30px;
    }

    .card {
      background-color: var(--card-bg);
      border-radius: 8px;
      border: 1px solid var(--border-color);
      padding: 20px;
      position: relative;
    }

    .card.red { border-left: 5px solid var(--accent-red); }
    .card.green { border-left: 5px solid var(--accent-green); }
    .card.cyan { border-left: 5px solid var(--accent-cyan); }

    .card h3 {
      margin-top: 0;
    }

    /* Blockquotes */
    blockquote {
      background-color: var(--card-bg);
      border-left: 4px solid var(--accent-cyan);
      padding: 12px 18px;
      margin-bottom: 15px;
      border-radius: 0 6px 6px 0;
    }

    blockquote p {
      margin-bottom: 6px;
      font-weight: 500;
    }

    blockquote p:last-child {
      margin-bottom: 0;
    }

    /* Tables */
    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 25px;
      background-color: var(--card-bg);
      border-radius: 6px;
      overflow: hidden;
    }

    th, td {
      border: 1px solid var(--border-color);
      padding: 12px 15px;
      text-align: left;
    }

    th {
      background-color: #21262d;
      color: var(--text-heading);
    }

    .grid-3 {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      margin-bottom: 25px;
    }

    .grid-card {
      background-color: var(--card-bg);
      border: 1px solid var(--border-color);
      border-radius: 8px;
      padding: 20px;
      text-align: center;
    }

    .grid-card h3 {
      border-bottom: 1px solid var(--border-color);
      padding-bottom: 10px;
      margin-bottom: 15px;
    }

    /* Resource Links */
    .resource-list {
      list-style: none;
      margin-left: 0;
    }

    .resource-list li {
      margin-bottom: 12px;
    }

    .resource-list a {
      text-decoration: none;
      display: inline-block;
    }

    /* Footer */
    .footer {
      text-align: center;
      margin-top: 40px;
      padding-top: 20px;
      border-top: 1px solid var(--border-color);
    }

    .author-box {
      background-color: var(--card-bg);
      border: 1px solid var(--border-color);
      border-radius: 8px;
      padding: 25px;
      text-align: center;
      max-width: 600px;
      margin: 0 auto 20px auto;
    }

    /* Code Syntax Highlighting Simulation */
    .keyword { color: #ff7b72; font-weight: bold; }
    .function { color: #d2a8ff; }
    .string { color: #a5d6ff; }
    .comment { color: #8b949e; font-style: italic; }
  </style>
</head>
<body>

<div class="container">

  <!-- HEADER -->
  <div class="header-banner">
    <img
      src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,45:1E293B,75:334155,100:00C2FF&height=260&section=header&text=🎵%20Music%20Store%20Analysis&fontSize=46&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Turning%20Music%20Store%20Data%20Into%20Business%20Insights&descAlignY=65&descSize=17"
      alt="Music Store Analysis Banner"
    />
  </div>

  <p class="subtitle">
    An end-to-end SQL Data Analytics project focused on customer behaviour,
    sales performance, music preferences, revenue analysis and geographic insights.
  </p>

  <!-- ACTION BUTTONS -->
  <div class="badge-group">
    <a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL" target="_blank">
      <img src="https://img.shields.io/badge/📂%20VIEW%20REPOSITORY-181717?style=for-the-badge&logo=github&logoColor=white" alt="View Repository" />
    </a>
    <a href="https://www.linkedin.com/in/keshavkapil15/" target="_blank">
      <img src="https://img.shields.io/badge/💼%20LINKEDIN-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
    </a>
  </div>

  <!-- TECH STACK BADGES -->
  <div class="badge-group">
    <img src="https://img.shields.io/badge/SQL-Data%20Analytics-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL" />
    <img src="https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
    <img src="https://img.shields.io/badge/pgAdmin4-Database%20Analysis-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="pgAdmin4" />
    <img src="https://img.shields.io/badge/Data%20Analytics-Business%20Insights-00A86B?style=for-the-badge" alt="Data Analytics" />
  </div>

  <!-- SQL CONCEPTS BADGES -->
  <div class="badge-group">
    <img src="https://img.shields.io/badge/JOINS-Advanced-FF8C00?style=for-the-badge" alt="Joins" />
    <img src="https://img.shields.io/badge/SUBQUERIES-SQL-8A2BE2?style=for-the-badge" alt="Subqueries" />
    <img src="https://img.shields.io/badge/CTEs-SQL-007ACC?style=for-the-badge" alt="CTEs" />
    <img src="https://img.shields.io/badge/WINDOW%20FUNCTIONS-SQL-E53935?style=for-the-badge" alt="Window Functions" />
  </div>

  <hr>

  <!-- PROJECT OVERVIEW -->
  <section>
    <h2>🎧 PROJECT OVERVIEW</h2>
    <div class="badge-group" style="justify-content: flex-start;">
      <img src="https://img.shields.io/badge/DATA%20→%20SQL%20→%20ANALYSIS%20→%20INSIGHTS-00E5FF?style=for-the-badge" alt="Workflow Badge" />
    </div>
    <p>
      <strong>Music Store Analysis</strong> is an end-to-end <strong>SQL Data Analytics project</strong> built around a relational music-store database.
    </p>
    <p>
      The project takes structured transactional and catalogue data and uses SQL to investigate business questions related to:
    </p>
    <p><strong>Customer Spending • Sales Performance • Music Preferences • Artists • Genres • Revenue • Geographic Demand</strong></p>

    <h3>Analytical Workflow</h3>
    <div class="ascii-diagram">UNDERSTAND THE DATA
       ↓
ASK BUSINESS QUESTIONS
       ↓
QUERY THE DATABASE
       ↓
ANALYZE THE RESULTS
       ↓
EXTRACT BUSINESS INSIGHTS</div>
  </section>

  <hr>

  <!-- EXECUTIVE CARDS -->
  <section class="card-section">
    <div class="card red">
      <h2>🔴 01 — PROBLEM STATEMENT</h2>
      <p>A digital music store generates information across multiple interconnected entities such as <strong>customers, invoices, invoice lines, tracks, albums, artists, genres, employees and playlists.</strong></p>
      <p>While the database contains a large amount of transactional and catalogue information, raw records alone do not directly answer important business questions.</p>
      <p>The analytical challenge is to transform this relational data into meaningful information around <strong>customer purchasing behaviour, sales performance, music preferences, artist popularity and geographic demand.</strong></p>
      <p>This project addresses that challenge through structured SQL analysis, connecting related tables and converting database records into measurable business insights.</p>
    </div>

    <div class="card green">
      <h2>🟢 02 — APPROACH</h2>
      <p>The project follows a structured <strong>end-to-end SQL analytics workflow</strong> rather than treating SQL as simply a query-writing exercise.</p>
      <p>The database is explored using SQL concepts ranging from fundamental data retrieval and filtering to advanced relational analysis.</p>
      <p>The analysis makes use of concepts including <strong>SELECT, WHERE, ORDER BY, GROUP BY, aggregate functions, JOINs, subqueries, nested queries, CTEs and window functions.</strong></p>
      <p>The questions progress from basic database exploration towards deeper business analysis involving <strong>customer spending, sales, genres, artists and geographic purchasing behaviour.</strong></p>
      <p>The final objective is to connect query results back to the original business question and interpret what the data is actually showing.</p>
    </div>

    <div class="card cyan">
      <h2>🔵 03 — FINDINGS</h2>
      <p>The analysis extracts business-oriented insights from the music-store database across multiple dimensions.</p>
      <p>The project investigates <strong>high-value customers, purchasing activity, revenue distribution, popular genres, artist activity and geographic purchasing patterns.</strong></p>
      <p>Advanced SQL analysis can be used to examine questions such as the <strong>most popular genre within a country</strong> and the <strong>highest-spending customer within a country.</strong></p>
      <p>The resulting analysis demonstrates how relational data can be transformed from individual database records into structured information that is easier to interpret from a business perspective.</p>
    </div>
  </section>

  <hr>

  <!-- BUSINESS QUESTIONS -->
  <section>
    <h2>💡 WHAT DOES THIS PROJECT ACTUALLY DO?</h2>
    <p>Imagine a digital music store containing information about thousands of:</p>
    <p><strong>Customers • Invoices • Tracks • Albums • Artists • Genres • Employees • Playlists</strong></p>
    <p>The database contains the information, but business questions require analysis. For example:</p>

    <blockquote>
      <p>🎯 <strong>Who spends the most?</strong></p>
      <p>💰 <strong>Which customers contribute the most revenue?</strong></p>
      <p>🎵 <strong>Which genres are most popular?</strong></p>
      <p>🎸 <strong>Which artists have the largest number of tracks?</strong></p>
      <p>🌍 <strong>Which countries generate the most purchasing activity?</strong></p>
      <p>👤 <strong>Who is the highest-spending customer in each country?</strong></p>
    </blockquote>

    <p>This project uses <strong>SQL as the analytical layer</strong> between the raw relational data and these business questions.</p>
  </section>

  <hr>

  <!-- DATABASE STRUCTURE -->
  <section>
    <h2>🗄️ DATABASE STRUCTURE</h2>
    <p>The Music Store database is based on interconnected relational entities.</p>
    
    <div class="ascii-diagram">                         🎵 MUSIC STORE DATABASE
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
                      🔗 PLAYLIST TRACK</div>

    <h3>🖼️ DATABASE SCHEMA</h3>
    <p style="text-align: center;">
      <img src="https://user-images.githubusercontent.com/112153548/213707717-bfc9f479-52d9-407b-99e1-e94db7ae10a3.png" alt="Music Store Database Schema" style="max-width: 100%; border-radius: 6px; border: 1px solid var(--border-color);" />
      <br>
      <strong>Music Store Relational Database Schema</strong>
    </p>

    <h3 style="margin-top: 30px;">📊 ANALYTICAL DOMAINS</h3>
    <div class="grid-3">
      <div class="grid-card">
        <h3>👥 CUSTOMER</h3>
        <p>Customer behaviour, spending and purchasing patterns.</p>
        <p><strong>Spending<br>Purchases<br>Revenue Contribution<br>Country-level Customers</strong></p>
      </div>
      <div class="grid-card">
        <h3>💰 SALES</h3>
        <p>Revenue and purchasing activity across the store.</p>
        <p><strong>Invoices<br>Revenue<br>Purchasing Activity<br>Geographic Sales</strong></p>
      </div>
      <div class="grid-card">
        <h3>🎵 MUSIC</h3>
        <p>Analysis of the music catalogue and customer preferences.</p>
        <p><strong>Genres<br>Artists<br>Tracks<br>Albums</strong></p>
      </div>
    </div>

    <h3>🌍 GEOGRAPHIC ANALYSIS</h3>
    <p>The relational structure also enables analysis from a geographic perspective:</p>
    <div class="ascii-diagram">🌎 Revenue by Country ──► 👥 Customer Distribution ──► 💰 Purchasing Behaviour ──► 🎵 Popular Genres ──► 👤 Highest-Spending Customers</div>
  </section>

  <hr>

  <!-- SQL CONCEPTS USED -->
  <section>
    <h2>🧠 SQL CONCEPTS USED</h2>

    <h3>01 — Fundamental SQL</h3>
    <p><code>SELECT</code> • <code>FROM</code> • <code>WHERE</code> • <code>ORDER BY</code> • <code>GROUP BY</code> • <code>DISTINCT</code> • <code>LIMIT</code></p>

    <h3>02 — Aggregate Functions</h3>
    <p><code>COUNT()</code> • <code>SUM()</code> • <code>AVG()</code> • <code>MIN()</code> • <code>MAX()</code></p>
    <div class="ascii-diagram"><span class="keyword">SELECT</span>
    country,
    <span class="function">SUM</span>(total) <span class="keyword">AS</span> revenue
<span class="keyword">FROM</span> invoice
<span class="keyword">GROUP BY</span> country;</div>

    <h3>03 — JOINs</h3>
    <div class="ascii-diagram"><span class="keyword">SELECT</span>
    c.first_name,
    c.last_name,
    i.total
<span class="keyword">FROM</span> customer c
<span class="keyword">JOIN</span> invoice i
    <span class="keyword">ON</span> c.customer_id = i.customer_id;</div>

    <h3>🔗 RELATIONAL ANALYSIS</h3>
    <div class="ascii-diagram">CUSTOMER
   │ (customer_id)
   ▼
INVOICE
   │ (invoice_id)
   ▼
INVOICE LINE
   │ (track_id)
   ▼
TRACK ──► ALBUM ──► ARTIST
   │
   └──► GENRE</div>

    <h3>🧩 SUBQUERIES</h3>
    <div class="ascii-diagram">MAIN QUESTION ──► SUBQUERY ──► CALCULATED VALUE ──► FINAL RESULT</div>

    <h3>🏗️ COMMON TABLE EXPRESSIONS (CTEs)</h3>
    <div class="ascii-diagram"><span class="keyword">WITH</span> customer_sales <span class="keyword">AS</span>
(
    <span class="keyword">SELECT</span>
        customer_id,
        <span class="function">SUM</span>(total) <span class="keyword">AS</span> total_spent
    <span class="keyword">FROM</span> invoice
    <span class="keyword">GROUP BY</span> customer_id
)
<span class="keyword">SELECT</span> * <span class="keyword">FROM</span> customer_sales;</div>

    <h3>🪟 WINDOW FUNCTIONS</h3>
    <p><code>ROW_NUMBER()</code> • <code>RANK()</code> • <code>DENSE_RANK()</code> • <code>SUM() OVER()</code> • <code>AVG() OVER()</code></p>
  </section>

  <hr>

  <!-- BUSINESS QUESTIONS TABLE -->
  <section>
    <h2>🎯 BUSINESS QUESTIONS</h2>
    <table>
      <thead>
        <tr>
          <th>Category</th>
          <th>Key Questions Addressed</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>👥 Customer Analysis</strong></td>
          <td>
            • Who is the highest-spending customer?<br>
            • Which customers contribute the most revenue?<br>
            • Who is the highest-spending customer in each country?<br>
            • How does customer purchasing behaviour vary?
          </td>
        </tr>
        <tr>
          <td><strong>💰 Sales Analysis</strong></td>
          <td>
            • Which countries generate the most revenue?<br>
            • What is the purchasing activity across regions?<br>
            • Which customers contribute most to sales?<br>
            • How is revenue distributed?
          </td>
        </tr>
        <tr>
          <td><strong>🎵 Music Analysis</strong></td>
          <td>
            • Which genres are most popular?<br>
            • Which artists have the most tracks?<br>
            • Which tracks have the longest duration?<br>
            • What patterns exist in customer music preferences?
          </td>
        </tr>
        <tr>
          <td><strong>🌍 Geographic Analysis</strong></td>
          <td>
            • Which countries have the highest purchasing activity?<br>
            • Which genre is most popular within a country?<br>
            • Who is the highest-spending customer within each country?
          </td>
        </tr>
      </tbody>
    </table>
  </section>

  <hr>

  <!-- TECH STACK -->
  <section>
    <h2>🛠️ TECHNOLOGY STACK</h2>
    <div class="badge-group" style="justify-content: flex-start;">
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
      <img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL" />
      <img src="https://img.shields.io/badge/pgAdmin4-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="pgAdmin4" />
      <img src="https://img.shields.io/badge/Data%20Analytics-00A86B?style=for-the-badge" alt="Data Analytics" />
      <img src="https://img.shields.io/badge/Business%20Insights-00B8D4?style=for-the-badge" alt="Business Insights" />
    </div>

    <table>
      <thead>
        <tr>
          <th>Technology</th>
          <th>Role</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>🐘 <strong>PostgreSQL</strong></td>
          <td>Relational database engine</td>
        </tr>
        <tr>
          <td>💻 <strong>SQL</strong></td>
          <td>Querying, transformation and analysis</td>
        </tr>
        <tr>
          <td>🖥️ <strong>pgAdmin 4</strong></td>
          <td>Database management and SQL execution</td>
        </tr>
        <tr>
          <td>📊 <strong>Data Analytics</strong></td>
          <td>Business-question-driven analysis</td>
        </tr>
      </tbody>
    </table>
  </section>

  <hr>

  <!-- REPOSITORY RESOURCES -->
  <section>
    <h2>📁 REPOSITORY RESOURCES</h2>
    <ul class="resource-list">
      <li>
        <a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/tree/main/DataAnalyst-Question" target="_blank">
          <img src="https://img.shields.io/badge/📋%20OPEN-DATA%20ANALYST%20QUESTIONS-FF6B35?style=for-the-badge" alt="Data Analyst Questions" />
        </a>
        <br><small>Questions that define the analytical problems addressed by the project.</small>
      </li>
      <li>
        <a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/tree/main/DataSet_CSV" target="_blank">
          <img src="https://img.shields.io/badge/🗃️%20OPEN-DATASET%20CSV-00A86B?style=for-the-badge" alt="Dataset CSV" />
        </a>
        <br><small>CSV-based dataset resources used as part of the project.</small>
      </li>
      <li>
        <a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/tree/main/SQL-File-DataSet" target="_blank">
          <img src="https://img.shields.io/badge/💻%20OPEN-SQL%20FILES-4169E1?style=for-the-badge" alt="SQL Files" />
        </a>
        <br><small>SQL/database resources used for querying and analysing the Music Store data.</small>
      </li>
      <li>
        <a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/blob/main/Music_Store-DataAnalysis-Report.pdf" target="_blank">
          <img src="https://img.shields.io/badge/📄%20VIEW-DATA%20ANALYSIS%20REPORT-E53935?style=for-the-badge" alt="Report PDF" />
        </a>
      </li>
      <li>
        <a href="https://github.com/keshavkapill/MUSIC-STORE-ANALYSIS-BY-SQL/blob/main/Music_Store-DataAnalysis-Report.pptx" target="_blank">
          <img src="https://img.shields.io/badge/📊%20VIEW-PROJECT%20PRESENTATION-8A2BE2?style=for-the-badge" alt="Presentation PPTX" />
        </a>
      </li>
    </ul>
  </section>

  <hr>

  <!-- STEPS -->
  <section>
    <h2>🚀 HOW TO EXPLORE THE PROJECT</h2>
    <ul>
      <li><strong>STEP 01 — Understand the Questions:</strong> Start inside <code>DataAnalyst-Question/</code> to review business problems.</li>
      <li><strong>STEP 02 — Understand the Dataset:</strong> Explore <code>DataSet_CSV/</code> to understand entity attributes.</li>
      <li><strong>STEP 03 — Understand the Database:</strong> Review SQL scripts inside <code>SQL-File-DataSet/</code>.</li>
      <li><strong>STEP 04 — Execute SQL Analysis:</strong> Use PostgreSQL / pgAdmin 4 to run queries.</li>
      <li><strong>STEP 05 — Interpret Results:</strong> Connect query outputs back to real business strategy.</li>
      <li><strong>STEP 06 — Review the Final Analysis:</strong> Open the PDF report or PPTX presentation deck.</li>
    </ul>
  </section>

  <hr>

  <!-- FOOTER -->
  <footer class="footer">
    <div class="author-box">
      <img src="https://img.shields.io/badge/KESHAV%20KAPIL-Data%20Analytics%20%7C%20SQL%20%7C%20Cloud-00E5FF?style=for-the-badge" alt="Author Badge" />
      <h3 style="margin-top: 15px;">BTech Computer Science Engineering</h3>
      <p>SQL • Data Analytics • Cloud • Full-Stack Development</p>
      
      <div class="badge-group" style="margin-top: 15px;">
        <a href="https://github.com/keshavkapill" target="_blank">
          <img src="https://img.shields.io/badge/GitHub-KESHAVKAPILL-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
        </a>
        <a href="https://www.linkedin.com/in/keshavkapil15/" target="_blank">
          <img src="https://img.shields.io/badge/LinkedIn-KESHAVKAPIL15-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
        </a>
      </div>
    </div>

    <div class="badge-group">
      <img src="https://img.shields.io/badge/🎵%20TURNING%20DATA%20INTO%20INSIGHTS-ONE%20QUERY%20AT%20A%20TIME-00E5FF?style=for-the-badge" alt="Tagline" />
    </div>

    <p><strong>Made with ❤️ by Keshav Kapil</strong></p>
  </footer>

</div>

</body>
</html>
