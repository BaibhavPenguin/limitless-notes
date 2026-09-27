# Introduction to DBMS &mdash; Module 1

## <u>Definition of Database </u>
**A Database is a collection of related data**. Here, data means a known fact , for example a
number which represents a telephone number or unique identification number, etc. **Data is fundamentally different from information, any data is a raw fact** while any information is data which has contextual meaning and/or application.  

**Example:** the number 34 by itself is data, it can represent anything age , distance , waiting time in a queue however, when it is attached with fields like age , distance , etc. We can instantly decipher its meaning thus it becomes information.

## <u>Database Management System (DBMS) </u>

A Database Management System (DBMS) is system software which manages the data. It can perform various tasks like creation, retrieval, insertion, modification and deletion of data to manage it in a systematic way as per requirement.

Databases are designed to manage large amounts of data by providing security from accidental crash of system and unauthorized access. DBMS provides a convenient and efficient environment which is used to handle the data.

**Example:** MySQL is a Database Management System.

---
**A Database Management System** is a computerized system that enables users to create , read, update and delete the records from a database thereby allowing them to manage and maintain a database throughout its functional lifetime. 
The DBMS is a general purpose software system which facilitates the process of **defining, constructing, manipulating and sharing** databases among various users and applications.


#### Defining a Database
Defining a database involves specifying the data types , structures and constraints of the data to be stored in the database. The schema (formal structure) of the database is created in this stage.
The database descriptive and definition information is also stored as metadata or db catalog 

#### Constructing the Database
Constructing the database is the process of strong the data on some storage medium that is controlled by the DBMS

#### Manipulating the Database
Manipulating the database includes functions such as querying the database to retrieve specific data, updating the database to reflect changes in the UoD and generating reports from the data.

#### Sharing a Database
Sharing a Database allows multiple users and programs to access the database simultaneously

### Query & Transaction
An application program accesses the database by sending queries or conducting transactions.

A **query** typically causes some data to be retrieved while a transaction may cause read and write
of some data. **A Query is a single request to the database** , it can either Create , Read , Update or Delete any data from the database while a **transaction is a logical sequence of queries** which can perform
multiple different operations in the given sequence.

## <u>Characteristics of DBMS</u>

The following are some characteristics of a Database Management System.

### Data Integrity
- Changes made to the database by authorized users should be prevented from affecting the accuracy and consistency of the data by implementing integrity restrictions.
- The accuracy and completeness of the data stored in a database are paramount to its integrity.
- This goal is never guaranteed, as it is impossible to guarantee the accuracy of each and every database record.

### Security
- There should be restrictions on how users can access the database.
- Users' ability to make changes to a database should be restricted, and they shouldn't have full access to the database.
- The Database shouldn't be accessible to unauthorized people.
- The DBMS provides multiple user authentication which relates directly to the user's access limit to the database.

### Real World Entity
- The most significant and easily understandable feature of DBMSs (Database Management Systems) is their actuality. Large corporate organizations can be managed using the Database Management System (DBMS), which is designed to securely store their company data.
- The cost of bread, milk, veggies, and other items can all be stored in the database. The entities in DBMSs (Database Management Systems) reflect actual entities in the real world.

### Self-Explaining Nature
- A database in a database management system (DBMS) contains another database, and that other database contains metadata as well.
- In this context, "metadata" refers to data about data.
- Metadata includes things like the name of the table and the total number of entries in a school database.
- Because of its self-explanatory nature, the database can automatically explain every piece of information. This is due to the fact that all of the data in the database is kept in an organized manner.

### Can store any kind of structured data
- Data can be stored in a structured fashion in a database.
- Any kind of real-world data can be stored in DBMSs and is organized in a structured manner.

### Ease of Access
- Any type of stored data in DBMS can be searched by using an easy search operation query. When compared to manual searching, it is far faster.
- All query types in the database can be implemented using the CRUD operation in DBMSs **(CRUD stands for Create, Read, Update, and Delete).**

### SQL & NoSQL Databases
- SQL and No-SQL are the two categories of databases (not DBMS).
- The data is kept in SQL databases as tables, or rows and columns. - Other than that, No-SQL databases can store data in any format. As an example, the widely used MongoDB database stores its data in JSON (JavaScript Object Notation) format.
- Because DBMS enables us to do operations on both types of databases, this is a feature of DBMS. Thus, we are able to perform operations and queries on both SQL and No-SQL databases.

**SQL Databases are formally called Relational Databases while NoSQL Databases are formally called Non&mdash;Relational Databases**

> NoSQL Databases are used for storing abstract data where relations aren't necessary.

## <u>Advantages of DBMS</u>

The following are some advantages of using **A Database Management System** over a traditional file system.

#### 1 &mdash; Controlling Data Redundancy
In File Processing System the different applications has separate files for data storage. In this case, the duplicated copies of the same data are created at many places.  
In DBMS, all the data of an organization is integrated into a single database, the data is recorded at only one place in the database and it is not duplicated.  

When they are converted into database, the data is integrated into a single database so that multiple copies of the same data are reduced to single-copy.  
Controlling the data redundancy helps to save storage space. Similarly, it is useful for retrieving data from database users.  

**Example:** The Employee file and the Team file contain several items that are identical.

#### 2 &mdash; Data Consistency
The data consistency is obtained by controlling the data redundancy, if a data item appears only once, any update to its value has to be performed only once and the updated value is immediately available to all users.

**Example:** If there is change in designation of employee, then the changes are made in single centralized file which is available to all the users.

#### 3 &mdash; Sharing of Data
In DBMS, data can be easily shared by different applications. The database administrator manages the data and gives rights to users to access the data.  
Multiple users can be authorized to access the same data simultaneously. The remote users can also share the same data.

#### 4 &mdash; Data Independence
In DBMS we can completely separate the data structure of database and programs or applications which are used to access the data.
This is called as data independence.   
If any changes are made in structure of database then there is no need to make changes in the programs.

**Example:** You can modify the size or data type of a data items (fields of a database table) without making any change in application program.

#### 5 &mdash; Data Control
The DBMS provides centralized data storage. Hence keeping control on data is very much easy as compared to Traditional File Processing System.  
As data is common for all the application, no possibility of any confusion or complication.

#### 6 &mdash; Security

In DBMS the different users can have different levels of access to data based on their roles. In the college database, students will have access to their own data only, while their teachers will have access to data of all the students whom they are teaching. 

**Example:** Class teacher will be able to see the reports of all the students in that class, but not other classes while, The principal will have access to entire data.  

Similarly, in a banking system, individual operator and clerk will have limited access to the data while the bank manager can access the entire data.  
All these levels of security and access are not allowed in file system.

#### 7 &mdash; Concurrency Control

In a computer file-based system, if multiple users are accessing data simultaneously, it is possible that it may lead to some irrelevant data generation. For example, if update operation is executed by both the users on the same record, then value updated by one may get overwrite by other.

Mostly the database management systems have sub-systems to control the concurrency so that accuracy is maintained in transaction recording.

#### 8 &mdash; Data Modelling of Real World

The DBMS has many functionalities are provided to represent the complex data and interfile relationships.  
This helps to map the database with real world applications.

## <u>Levels of Abstraction</u>

To make the user interaction easy with the database, the internal irrelevant details can be hidden from users.  
**This process of hiding irrelevant details from users is called data abstraction.**
The complexity of the database can be hidden from the user by different levels of abstraction.

There are three levels of abstraction namely, Physical Level, Logical Level, View Level

<figure>
<img src="https://i.postimg.cc/K886Vxhg/image1.png">
<figcaption align="center">Levels of Abstraction</figcaption>
</figure>

### <u>View (External) Level</u>
The View (External) Level is the highest level of abstraction. It defines how the end-users interact with the database, how they can see the database and which information of the database they have access to. Different views are used to hide unnecessary data from users and provide a customised view to relevant data. It improves security as confidential data can be hidden and only made visible to authorized users. It also simplifies database usage.

### <u>Logical Level (Conceptual Level)</u>

The Logical Level describes the entire structure (schema) of a database. It defines what data is stored and the relationships amongst the data but not how it is stored on physical hardware. It includes Tables, Attributes (Columns) , Fields (Rows) , Keys and Relationships.
Database designers work at the Logical Level , this level maintains relationships between data while making it easier to design a database and perform operations like create , read, update delete on the database.

### <u>Physical Level (Internal Level)</u>
The Physical Level describes how the data is actually stored on hardware. Only the DBMS and the Database Administrator (DBA) has direct access to the Physical Level, It includes Files, Blocks, Storage Hardware, Data Redundancy, Buffer Management, Complex and Efficient Data Structures, etc.

## <u>Data Independence</u>

### <u>Physical Data Independence</u>
The ability to modify the internal schema without requiring modifications to the conceptual schema is known as physical data independence.  
The conceptual structure of the database will remain unaffected by any modifications we make to the database system server's storage capacity.
Conceptual and internal levels are separated by physical data independence.  

### <u>Logical Data Independence</u>
It refers to the ability to change the logical schema without disrupting the application program or external schema.  
Any modifications made to the conceptual view of the data would not impact the user view of the data.
These modifications could involve adding or removing attributes, changing entities or relationships in table structures to the logical schema, etc.

## <u>Data Architecture</u>
DBMS (Database Management System) acts as an interface between the user and the database.  
The user requests the DBMS to perform various operations (retrieve, insert, delete and update) on the database.

### <u>Structure of Database</u>

#### 1 &mdash; DDL Compiler
The DDL Compiler converts DDL commands into set of tables containing metadata stored in a data dictionary.

#### 2 &mdash; DML Compiler & Query Optimizer
The DML commands such as retrieve, insert, update, delete etc. from the application programs are sent to the DML compiler for compilation. It converts these commands into object code for understanding of database.  
The object code is then optimized in the best way to execute a query by the query optimizer and then send to the data manager.

#### 3 &mdash; Data Manager
The Data Manager is the central software component of the DBMS also knows as Database Control System.  
The main functions of the Data manager are:
- It converts the requests received from query optimizer to machine understandable format. It makes actual request inside the database.
- Controls DBMS information access that is stored on disk.
- It controls and handles buffers in main memory.
- It enforces constraints to maintain consistency and integrity of the data.
- It synchronizes the simultaneous operations performed by the concurrent users.
- It also controls the backup and recovery operations.

#### 4 &mdash; Data Dictionary

Data Dictionary is a repository of description of data in the database. It contains metadata that is information about data.  
It stores data like - names of the tables, names of attributes of each table, length of attributes, and number of rows in each table.  

Constraints on data i.e. range of values permitted.
Detailed information on physical database design such as storage structure, access paths, files and record sizes.  

Access Authorization - is the Description of database users their responsibilities and their access rights.
Usage statistics such as frequency of query and transactions.  

Data dictionary is used to actually control the data integrity and accuracy. It may be used as an important part of the DBMS.

**Importance of Data Dictionary**  
Data Dictionary is necessary in the databases due to following reasons :

- It improves the control of DBA over the information system and user's understanding for the use of the system.

- It helps in documenting the database design process by storing documentation of the result of every design phase and design decisions.

- It helps in searching the views on the database definitions.

- It provides great assistance in producing a report of which data elements (i.e. data values) are used in all the programs.

#### 5 &mdash; Data File
It contains the data portion of the database i.e. it has the real data stored in it.  
It can be stored as magnetic disks, magnetic tapes or optical disks.  
In the modern day, Hard Disk Drives and Solid State Drives are used for storing Data Files as they provide high speed and reliability while requiring less operational power.

#### 6 &mdash; Compiled DML
The DML compiler converts the high level queries into low level file access commands known as compiled DML.  
Some of the processed DML statements (insert, update, delete) are stored in it so that if there is similar requests, the data can be reused.

#### 7 &mdash; End Users
They are the real users of the database.  
They can be developers, designers, administrator or the actual users of the database.

*&mdash; Edited by Baibhav Bhattacharya & Prem Vishwakarma*
