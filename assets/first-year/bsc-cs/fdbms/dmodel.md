# Data Models &mdash; Module 1

## <u>Client &mdash; Server Architecture</u>

Vendor-provided applications (often called tools) are applications whose basic purpose is to assist in the creation and execution of other applications.  

**Example:** one of the vendor-provided tools will be a report writer, whose purpose is to allow end users to obtain formatted reports from the system on request.  

Any given report request can be regarded as a small application program, written in a very high level report writer language.

#### Vendor provided tools can be divided into several more or less distinct classes &mdash; 

-  Query language processors

- Report writers

- Business graphics subsystem

- Spreadsheets

- Natural language processors

- Statistical packages

- Copy management or "data extract" tools

- Application generator (including 4 GL processors)

- Other application development tools including computer-aided software engineering (CASE) products.

- Data mining and visualization tools and many others.
 
Since the overall system system can be so neatly divided into two parts, server and clients, the possibility arises of running the two on different machines.  
In other words, the potential exists for distributed processing.
Distributed processing means that distinct machines can be connected into some kind of communication network in such a way that a single data processing task can be spread across several machines in the network.

Since, Client&mdash;Server Architectures are convenient and secure, almost all modern applications rely on it for deployment and maintenance.

## <u>Data Models</u>

**The data model is the fundamental structure or layout of the database.
A set of conceptual tools for characterizing data, data relationships, data semantics, and consistency constraints is called a data model.**  

The fundamental structure of a database is described by its data model.
The Data Model gives us an idea of how the final system will look after its complete implementation.  

It helps to design a database at **Physical**, **Logical** and **View level**. Data models can be classified in two ways:  

### <u>Object Based Logical Model</u>
Data is described at the logical and view levels by object-based logical models. It's capable of flexible structuring. It allows specifying data constraints explicitly Under Object-based logical model there are following data model:  

### <u>Entity Relationship Model (ER Model)</u> 
The ER model is a high-level data model that is based on how the real world is perceived and is made up of relationships between various basic objects known as entities.  
An entity is a real-world thing or object that can be identified from other things.  
**Entities are described in the database by a set of attributes.**

### <u>Object Oriented Model</u> 
An addition to the ER model that includes concepts of object identification, encapsulation, and functions.  
This model supports a rich type system that includes structured and collection types, An object contains values stored in instance variables within the object. These values are themselves objects.  

**Example:** The object may contain instance variables account_number and total_balance.  
Every object has a distinct identity, unlike the entities in the E&mdash;R model. It is possible that the values it contains. Two objects containing the same values are distinct.

### <u>Record Based Logical Model</u> 

- Record based models are basically used to describe the external and Conceptual level of a database.  

- They can also be used to describe the Internal level to some extent.

- They are used to develop and specify the logical structure and provide options for implementation of the design.

- In a record-based data model, databases consist of different records.

- Records may be of different types.

- Each record type defines the Fixed number of fields.

- There are 3 types of record based data models:

    1. Hierarchical Model

    2. Network Model

    3. Relational Model

#### <u>Hierarchical Model</u>

- The hierarchical model arranges records in hierarchy like an organizational chart.

- Each record type in this model is called a node or segment.

- A node represents a particular entity.

- The top-most node is called root. Each node is a subordinate of the node that is at the next higher level.

**Example:** One department can have many courses, many professors and of-course many students.

#### <u>Features of Hierarchical Model</u>
1. **One to Many Relationship:** The data here is organized in a tree-like structure where the one-to-many relationship is between the data-types. Also, there can be only one path from parent to child.

2. **Parent Chile Relationship:** Each child node has a parent node but a parent node can have more than one child node. Multiple parents are not allowed.

3.  **Cascading Deletion** If a parent node is deleted then the child node is automatically deleted.

4. **Pointers:** Pointers are used to link the parent node with the child node and are used to navigate between the stored data.

#### <u>Advantages of Hierarchical Model</u>
1. It is very simple and fast to traverse through a tree-like structure.

2. Any change in the parent node is automatically reflected in the child node so the integrity of data is maintained.

#### <u>Disadvantages of Hierarchical Model</u>
1. Complex relationships are not supported.

2. As it does not support more than one parent of the child node so if we have some complex relationship where a child node needs to have two parent nodes then that can be represented using this model.
3. If a parent node is deleted then the child node is automatically deleted.

---

#### <u>Network Model</u>
The network model is similar to hierarchical models.

- The difference is that a child node can have more than one parent node.

- The child nodes are represented by arrows in the network model.

- It also provides more flexibility than hierarchical models.

- The main difference of the network model from the hierarchical model is its ability to handle many to many (n:n) relationships or in other words it allows a record to have more than one parent.

**Example:** There are relationships among courses offered and students enrolled for courses and each course may have a number of students enrolled for it. The students enrolled for English are Riya and Priyanka and Riya has taken three courses: English, Math and Science. While Priyanka has taken English, History & Psychology, thus the Riya and Priyanka can both select English while being from different courses

#### <u>Advantages of Network Model</u>
1. It is conceptually simple and easy to design.

2. It can handle one to many (1:n) and many to many (n:n) relationships.

3. The changes in data characteristics do not require changes to the application programs.

4. The data access is easier and flexible than the hierarchical model.

#### <u>Disadvantages of Network Model</u>
1. Detailed structured knowledge is required.

2. There is a lack of structural independence.

3. The insertion, deletion and updating operations of a record require a large number of pointer adjustments.

 
---

#### <u>Relational Model</u>

This model is mostly widely used by commercial data processing applications.

- This model was initially described by Edgar F. Codd in 1969.

- It uses a collection of tables for representing data and the relationships among those data.

- Data is stored in tables called Relation.

- Each table is a group of columns and rows, where the column represents the attribute of an entity and row represents records or tuples.

- Attribute or field : Each column in a relation is called an attribute. The values of the attribute should be from the same domain.

- Example we have different attributes of the student like Student_Id, Student_Name, Student_Age etc.

- Tuple or Record : Each row in the relation is called tuple. A tuple defines a collection of attribute values. So each row in a relation contains unique values.

- Example : Each row has all the information about any specific individuals like the first row has information about student Ashish.

- The following example demonstrates the Student table of Relational Model.

#### <u>Advantages of Relational Model</u>

1. Simple : This model is more simple as compared to the network and hierarchical model.

2. Scalable : This model can be easily scaled as we can add as many rows and columns we want.

3. Structural Independence : We can make changes in database structure without changing the way we access the data. When we can make changes to the database structure without affecting the capability of DBMS to access the data we can say that structural independence has been achieved.

#### <u>Disadvantages of Relational Model</u>
1. Hardware Overheads : For hiding the complexities and making things easier for the user this model requires more powerful hardware computers and data storage devices.

2. Bad Design : As the relational model is very easy to design and use. So the users don't need to know how the data is stored in order to access it. This ease of design can lead to the development of a poor database which would slow down if the database grows.

*&mdash; Edited by baibhav Bhattacharya & Prem Vishwakarma*