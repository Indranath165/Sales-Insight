<h1>Sales-Insight</h1>
Sales Insight is a data analysis project that provides insights and visualizations for sales data. It includes a SQL database file <b>(db.dump.sql)</b> and a Power BI dashboard for easy viewing of the data. Sales Insight is designed to analyze and visualize sales data, helping businesses gain valuable insights into their sales performance. By leveraging the provided SQL database and Power BI dashboard, users can explore the data, generate reports, and uncover trends and patterns.
<h2>Installation</h2>
To use Sales Insight, follow these steps:
<ol>
    <li>Clone or download this repository to your local machine.</li>
    <li>Import the SQL database file <b>(db.dump.sql)</b> into your preferred database management system. This will create the necessary tables and populate them with sample data.</li>
    <li>Install Power BI Desktop (if you haven't already) from the official Microsoft website: <a href="https://powerbi.microsoft.com/" target="_blank">https://powerbi.microsoft.com/</a></li>
    <li>Open Power BI Desktop and open the Sales Insight Power BI project file <b>(sales insights.pbix)</b> located in the cloned repository.</li>
    <li>Connect the Power BI dashboard to your SQL database by providing the necessary connection details (server, database name, credentials, etc.). Make sure to update the connection string in the Power BI project accordingly.</li>
    <li>Once the connection is established, you should be able to see the data and start exploring the Sales Insight dashboard.</li>
</ol>
<h2>Data Analysis Using SQL</h2>
1. Show all customer records <br> &nbsp &nbsp<code>SELECT * FROM customers;</code> <br>
2. Show total number of customers <br> &nbsp &nbsp<code>SELECT count(*) FROM customers;</code> <br>
3. Show transactions for Chennai market (market code for chennai is Mark001) <br> &nbsp &nbsp<code>SELECT * FROM transactions where market_code='Mark001';</code> <br>
4. Show distrinct product codes that were sold in chennai <br> &nbsp &nbsp<code>SELECT distinct product_code FROM transactions where market_code='Mark001';</code> <br>
5. Show transactions where currency is US dollars <br> &nbsp &nbsp<code>SELECT * from transactions where currency="USD";</code> <br>
6. Show transactions in 2020 join by date table <br> &nbsp &nbsp<code>SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;</code> <br>
7. Show total revenue in year 2020 <br> &nbsp &nbsp<code>SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";</code> <br>
8. Show total revenue in year 2020, January Month <br> &nbsp &nbsp<code>SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");</code> <br>
<h2>Usage</h2>
Sales Insight offers a user-friendly interface through the Power BI dashboard. Here are some tips on how to make the most of it: <br>
<ul>
    <li>Navigate through different pages and visualizations to explore various aspects of the sales data.</li>
    <li>Use filters and slicers to drill down into specific regions, time periods, products, or any other relevant dimensions.</li>
    <li>Interact with the charts and graphs to view additional details or summary information.</li>
    <li>Export or share the generated reports and visualizations with your team or stakeholders.</li>
</ul>
Feel free to customize and extend the Power BI dashboard to suit your specific needs.
<h2>Database</h2>
The SQL database file <b>(db.dump.sql)</b> contains the necessary schema and sample data for the Sales Insight project. It is recommended to import this file into your preferred database management system to replicate the project's environment.
<h2>Dashboard</h2>
The Sales Insight Power BI dashboard <b>(sales_insight.pbix)</b> provides an intuitive and interactive interface to analyze the sales data. It includes various visualizations, such as charts, graphs, and tables, to help you gain insights and spot trends.<br>
<br>Below are some key features of the dashboard:
<ul>
    <li>Overview page: Provides a high-level summary of sales performance, including total revenue, top-selling products, and regional distribution.</li>
    <li>Sales by Region: Visualizes sales data geographically, allowing you to identify the most lucrative regions and analyze their performance.</li>
    <li>Product Analysis: Offers detailed insights into product performance, such as sales by category, top-selling products, and revenue trends.</li>
    <li>Time Analysis: Allows you to explore sales patterns over time, including monthly, quarterly, and yearly trends.</li>
</ul>
<h2>Contributions</h2>
Contributions are welcome! We value your input and encourage you to actively participate in the project. If you have any ideas, suggestions, bug reports, or feature requests, please don't hesitate to open an issue on GitHub. Additionally, we appreciate any code contributions you may have. If you'd like to contribute code, please submit a pull request, and we will review it as soon as possible. Thank you for your support!
