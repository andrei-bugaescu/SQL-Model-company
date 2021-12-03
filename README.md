# SQL-Model-company

Model company - Dashboarding

Introduction

You are commissioned by a company selling models and scale models. The company already has a database that lists employees, products, orders, and much more. You are invited to browse and discover this database. The director of the company wishes to have a dashboard which he could refresh each morning to have the latest information in order to manage the company.

Objective

Your dashboard should revolve around these 4 main topics: sales, finance, logistics, and human resources.
Here are the indicators that should be present in your dashboard. Visualizations would also be appreciated. And you are invited to practice your advisory role, by proposing additional KPIs and charts.
Sales: The number of products sold by category and by month, with comparison and rate of change compared to the same month of the previous year.
Finances: 
The turnover of the orders of the last two months by country. 
Orders that have not yet been paid.
Logistics: The stock of the 5 most ordered products.
Human Resources: Each month, the 2 sellers with the highest turnover.

Resources

source : https://www.mysqltutorial.org for the schema, and lots of modifications for datas

Tools
The manager does not want to do SQL, he wants to be able to access the data automatically and graphically. You can therefore propose a tool of your choice, as long as the dashboard is relevant.

For information, the database is available on a company server. You can access it in read-only mode with a user provided below.
The company also provides you with the script that you can run on your local MySQL server. The data are identical, and it stops at the end of the previous month.
On the morning of the demo, the data will be refreshed with new and fresh data (and you will be able to receive the update script if you do it locally). The demo should therefore display the latest available data.


SQL Database
You have the choice between connecting to the cloud server, or deploy the script locally. Data are identical in both ways.

Local installation
You will install a MySQL Community server on your machine, as well as the MySQL Workbench client.
The database is ready to be loaded into a MySQL server. Connect to your server via Workbench, and run all of the code in this file.


Reporting tool
You can use the tool of your choice. For information, the company used LibreOffice Calc spreadsheet before, so if you want to use it, you can see the PrintScreen to connect it. To be more collaborative, we have some printscreens about connecting Google Data Studio to the cloud server. And of course, you can use beautiful reporting Business Intelligence tools like Tableau Software. It’s up to you to present the best possible dashboard on the tool of your choice.
Be careful : you chose your own reporting tool. But the goal is to practice SQL. So you need to get the data in SQL queries. For example, for the “2 sellers with the highest turnover for each month” : 
what we would like: a SQL query with only the “2 sellers with the highest turnover for each month”, and a dataviz to show this.
what we don't want: a SQL query with every seller, then filters in your reporting tool.



Expected Deliverables


You will give a short presentation of your dashboard (ask for the duration at your trainer).

Below : installation guide if needed

LibreOffice : installation example
You can download and install LibreOffice Calc spreadsheet. The dashboard will therefore be a LibreOffice Calc workbook, connected to the MySQL server, and distributed on several tabs by theme. The manager can then refresh the data when he wants.

In LibreOffice, launch "Base" and connect to the server, then follow the steps.


--------------------------------------------------------------------------------
If Libreoffice send you this error message : 

→ You have to execute this code in MySQL Workbench, then restart libreoffice :
ALTER USER 'user'@'address_IP_server' IDENTIFIED WITH mysql_native_password BY 'password';
--------------------------------------------------------------------------------



Click on “Create Query in SQL View” :

Select the last icon “Run SQL command directly”, so now you can write your own query, run the query (F5) and save it.


Remember to save the query AND the LibreOffice-Database 

Once your database is registered, you can use the data:
- NOT RECOMMENDED directly (but not dynamically) via the "View" menu, then "Data sources"
- RECOMMENDED dynamically by inserting a pivot table on an existing source : Menu insert → Pivot table :


Google Data Studio : connecting example
Connect on the Google Data Studio here, and create a new “blank report”

Search “mysql” and click on the good connector :

You can now authenticate, and write your own queries :



