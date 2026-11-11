-- Week 1 – Supabase SQL Practice --

During my first week, I started working with Supabase and PostgreSQL using the UrbanStyle training database.

Here are five SQL commands I practised.

**1. Create a table**

Create a table for team members if it does not already exist.

CREATE TABLE IF NOT EXISTS public.team_members (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    role VARCHAR(100),
    week INT DEFAULT 0,
    joined_at TIMESTAMP DEFAULT NOW()
);

**What I learned:** CREATE TABLE creates a database table. IF NOT EXISTS prevents an error if the table already exists.

**2. View all records**

Display all columns and records from the team_members table.

SELECT *
FROM public.team_members;

**What I learned:** SELECT * retrieves all columns from a table.

**3. Select specific columns**

Display customer ID, sale date and total price from the sales table.

SELECT customer_id, sale_date, total_price
FROM sales
LIMIT 20;

**What I learned:** I can select only the columns I need instead of displaying the entire table.

**4. Find the five largest sales**

Sort sales from highest to lowest.

SELECT sale_id, total_price AS summa
FROM sales
ORDER BY total_price DESC
LIMIT 5;

**What I learned:** ORDER BY sorts the results, DESC means descending order, and LIMIT 5 returns only five records. AS gives a column an alternative name.

**5. Find the five smallest sales**

Sort sales from lowest to highest.

SELECT sale_id, total_price AS summa
FROM sales
ORDER BY total_price ASC
LIMIT 5;

**What I learned:** ASC sorts results in ascending order, allowing me to find the smallest sales.

**Key SQL concepts practised**

CREATE TABLE – creating database tables.

SELECT – retrieving data.

FROM – choosing a table.

ORDER BY – sorting results.

ASC and DESC – ascending and descending order.

LIMIT – controlling how many rows are returned.

AS – renaming a column in query results.
