# DDL Statements &mdash; Module 1

## <u>DDL Statements</u>

- DDL Stands for **Data Definition Language**, it is used to define the structure or **schema** of the database.
- All DDL Statements are auto-committed i.e. the changes made by DDL Statements are saved permanently in the database.
- It deals with the creation, modification and deletion of Databases, Tables, Views, etc but NOT Data.
- These commands should only be used by the programmer working at the logical level and should remain hidden from the End Users at the View Level.

#### <u>List of DDL Statements</u>

- `CREATE` : This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).

- `DROP` :  This command is used to delete objects from the database and/or the database itself.

- `ALTER` : This is used to alter the structure of the database.

- `TRUNCATE` : This is used to remove all records from a table, including all spaces allocated for the records are removed.

- `COMMENT` : This is used to add comments to the data dictionary.

- `RENAME` : This is used to rename an object existing in the database.


## <u> Creating a Database </u>

To create a database, we use the `CREATE` DDL Statement with the `DATABASE` argument.  

### Syntax
`CREATE DATABASE <database_name>`

### Example
`CREATE DATABASE College`

## <u> Using a Database </u>

To run queries, we first need to tell the DBMS what database to run these queries on, hence we need to `USE <database_name>`   
This statement is required because a DBMS like MySQL Supports running queries on multiple databases.   

### Syntax
`USE <database_name>`

### Example
`USE College`

--- 

<div class="code-sandbox-wrapper mysql-sandbox-wrapper">
<div class="mysql-status-badge">
<span class="mysql-status-dot"></span>
<span class="mysql-status-text">Waiting</span>
</div>
<div class="mysql-island">
<div class="mysql-island-header">
<div class="mysql-header-left">
<span class="mysql-island-title">MySQL Sandbox</span>
</div>
</div>
<div class="mysql-island-body">
<!-- Output Window (Fixed height, scrollable terminal) -->
<div class="mysqlterm">
<pre class="mysql-output">Welcome to the Limitless MySQL monitor. Commands end with ;</pre>
</div>
<!-- Line Editor (Middle) -->
<div class="mysqlsource">
<textarea readonly class="mysql-line-edit" rows="1" spellcheck="false" placeholder="Enter SQL statements here (e.g. SHOW DATABASES;)..." oninput="autoExpandSQLEdit(this)" onkeydown="handleSQLKeyDown(event, this)">create database College;
use College;</textarea>
</div>
<!-- Bottom Actions Bar (Clean Clear & Red Enter Buttons) -->
<div class="mysql-island-footer">
<div class="mysql-footer-actions">
<button class="mysql-btn mysql-clear-btn" onclick="clearMySQLTerminal(this)">Clear</button>
<button class="mysql-btn mysql-enter-btn" onclick="runMySQLCode(this)">⏎ Enter</button>
</div>
</div>
</div>
</div>
</div>




