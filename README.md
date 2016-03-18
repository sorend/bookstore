# bookstore

This is a fork of [Sergey Kim's bookstore](https://github.com/srgykim/bookstore). Please see his project for updates and changes. Highlights of this fork are:

- Use H2 database instead of PostgreSQL.
- Use Eclipse for project instead of NetBeans.

## Getting started

1. Download and install latest Eclipse JavaEE (Mars.1 is what was used).

2. Open the project in Eclipse:

   a. File > Import > Git > Projects from Git
   b. Select: Clone URI
   c. Use URI: **git://github.com:sorend/bookstore**
   d. In the wizard for project import, select Import existing Eclipse projects

3. Start the H2 database server. It is available in the web/lib/ folder in this repository.

   cd web/lib/
   java -cp h2*.jar org.h2.tools.Server
   
4. Create the database in H2

   a. When the H2 server starts it opens a browser console. Connect to the database using the following JDBC url: **jdbc:h2:tcp://127.0.1.1/~/bookstore**  (leave other settings as default).
   b. In the H2 database console copy and paste the contents of bookstore.sql

5. Start web application in Eclipse: Right-click on project > Run As > Run on Server
