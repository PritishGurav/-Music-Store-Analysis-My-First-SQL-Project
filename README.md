<h1 align="center">🎵 Music Store Analysis — My First SQL Project</h1>

<p align="center">
  <em>Exploring data harmony through the rhythm of SQL queries 🎶</em><br>
  <strong>Tools Used:</strong> MySQL | SQL | Data Analysis | Database Design
</p>

---

<h2>📖 Project Overview</h2>

<p>
This project marks the <strong>beginning of my journey into data analytics</strong> — a hands-on exploration into the world of SQL.  
Using a simulated <strong>Music Store Database</strong> (similar to platforms like iTunes), I analyzed sales patterns, customer behaviors, and revenue performance to uncover actionable business insights.
</p>

<p>
The database consists of multiple interconnected tables — <strong>Customers</strong>, <strong>Invoices</strong>, <strong>Tracks</strong>, <strong>Albums</strong>, <strong>Artists</strong>, <strong>Genres</strong>, and <strong>Employees</strong>.  
Together, they form a complete ecosystem of a real-world digital music store, making it a perfect dataset for practicing data analysis and relational database concepts.
</p>

---

<h2>🎯 Objectives</h2>

<ul>
  <li>Understand database relationships and apply <strong>JOIN operations</strong> effectively.</li>
  <li>Retrieve, filter, and summarize sales and music-related data using <strong>SQL queries</strong>.</li>
  <li>Gain business insights such as top-selling genres, most loyal customers, and revenue-generating artists.</li>
  <li>Build a solid foundation in SQL for future data-driven projects.</li>
</ul>

---

<h2>🧠 Key Highlights</h2>

<ul>
  <li>Analyzed sales performance by customer, genre, and artist to identify revenue trends.</li>
  <li>Explored global purchasing patterns using advanced SQL functions and aggregations.</li>
  <li>Developed queries to rank top-performing tracks and albums based on sales frequency.</li>
  <li>Practiced <strong>data cleaning</strong> and <strong>query optimization</strong> for accurate results.</li>
  <li>Built a foundation for <strong>real-world business intelligence</strong> using structured data.</li>
</ul>

---

<h2>🧩 Sample SQL Queries</h2>

<pre>
-- 🎤 1️⃣ Find the total number of customers
SELECT COUNT(*) AS Total_Customers FROM customers;

-- 🎧 2️⃣ Identify the top 5 best-selling genres
SELECT g.name AS Genre, COUNT(t.track_id) AS Tracks_Sold
FROM tracks t
JOIN genres g ON t.genre_id = g.genre_id
JOIN invoice_items i ON i.track_id = t.track_id
GROUP BY g.name
ORDER BY Tracks_Sold DESC
LIMIT 5;

-- 🎸 3️⃣ Find the artist generating the highest revenue
SELECT a.name AS Artist, SUM(i.total) AS Total_Revenue
FROM invoices i
JOIN invoice_items ii ON i.invoice_id = ii.invoice_id
JOIN tracks t ON ii.track_id = t.track_id
JOIN albums al ON t.album_id = al.album_id
JOIN artists a ON al.artist_id = a.artist_id
GROUP BY a.name
ORDER BY Total_Revenue DESC
LIMIT 1;

-- 🎷 4️⃣ Show top 5 countries by total sales
SELECT billing_country, SUM(total) AS Revenue
FROM invoices
GROUP BY billing_country
ORDER BY Revenue DESC
LIMIT 5;
</pre>

---

<h2>📈 Insights Discovered</h2>

<ul>
  <li>🎶 <strong>Rock and Latin genres</strong> dominate the sales charts.</li>
  <li>💰 Certain artists consistently drive higher revenue across multiple albums.</li>
  <li>🌍 Sales distribution reveals strong performance in North American and European markets.</li>
  <li>🧑‍💼 Customer loyalty is directly linked with average invoice frequency and genre preference.</li>
</ul>

---

<h2>💡 Key Learnings</h2>

<ul>
  <li>Developed a strong foundation in <strong>SQL querying and database management</strong>.</li>
  <li>Learned how to connect business logic with raw data to form meaningful insights.</li>
  <li>Understood how <strong>data relationships</strong> drive business intelligence in real-world applications.</li>
  <li>Improved analytical thinking and attention to detail when working with relational databases.</li>
</ul>

---

<h2>🚀 Conclusion</h2>

<p>
The <strong>Music Store Analysis Project</strong> taught me how to transform a simple dataset into a story — 
where each query adds rhythm and structure to the melody of data.  
It marks the <strong>first step in my data analytics journey</strong>, blending curiosity, logic, and creativity through the art of SQL.
</p>

---

<h3 align="center">🎵 Composed and Coded by <a href="https://www.linkedin.com/in/pritish-gurav">Pritish Gurav</a> 🎵</h3>
