# Entity Relationship Model and ER Table

<link rel="stylesheet" href="./styles/tables.css">

## <u>Entity</u>
---

An entity is a thing that exists either physically or logically.

- An entity may be a physical object such as a house or a car, or an entity may be a logical concept like an event such as a house sale or a car service, or a concept such as a customer transaction or order.

- The E-R model consists of entities and relationships between those entities. An entity is nothing but a thing having its own properties.

- These properties help to differentiate the object (entity) from other objects.

- In the ER diagram, an entity can be represented as rectangles.

**Example:** In the following ER model the Employee and department are Entities.

## <u>Attributes</u>
---

**Attributes are the properties which define the entity type.**  
<u>Eclipse is used to represent an attribute.</u>   

**Example:** The Employee entity could use Employee id, Employee name and The Department entity could use Department number and Department name as attribute.

### <u>Types of Attributes</u>

**Simple Attribute:** It can not be divided into simpler components.  
**Example:** Gender of an Employee. Gender cannot be broken down into smaller parts.  

**Composite Attributes:** An attribute composed of many other attribute is called as composite attribute.  
**Example:** Address attribute of Employee Entity type consists of Street, City, State, and Country. In ER diagram, composite attribute is represented by an oval comprising of ovals.  

**Multi-valued Attributes:** The attribute having many values for a particular entity is called as multi-valued attribute.  
**Example:** Each Employee has multiple mobile numbers.  

**Derived Attribute:** The value of this attributes which can be derived from the value of related stored attribute which are known as derived attribute.  
**Example:** The First Name & Last Name can be derived from the Full Name of a customer.  

**Key Attribute:** An attribute of an entity type for which each entity must have a unique value is called a key attribute of the entity type. **Key attributes are also called as Super Keys**  
**Example:** StudentId of each student in a college is unique.  

**Null Attributes:** This attribute can take NULL value when entity does not have value for it.  
**Example:** Before any exams are conducted, the result attribute of a student may show NULL to indicate that data does not exist.

**Stored Attributes:** The attribute that need to be stored permanently in database.  
**Example:** Date of joining of Employee is stored permanently.

  
<div class="dyntable">
<table>
<tr>
<th>Type </th>
<th> Notation </th>
</tr>

<tr>
<td>Attribute (Simple/Single valued/Stored)
<td>Key attributes
</tr>

<tr>
<td>Oval notation
<td>Oval with underline
</tr>

</table>
</div>


## <u>Keys</u>
---
Keys are used for uniquely identifying a row in a table and form different types of relationships between two or more tables.  
The following are the different types of keys.  

#### Super Key
Any attribute that can uniquely identify a row is called a super key or a key attribute

#### Candidate Key
Anything that uniquely identifies a row without any redundant attributes is called a Candidate Key, Candidate Keys are also called **Minimal Super Keys**  

#### Composite Key
Anything which is made using combination of two or more columns/attributes (like {name,age}) and can uniquely identify a row is called a composite key  

*Not all composite keys are candidate keys, for example - In the composite key {StudentUID,StudentName} StudentUID can identify all students independently, thus the student name is redundant and unnecessary, hence this composite key is NOT a candidate key*

#### Primary Key
The candidate key selected to uniquely identify the row by default. It has to be unique and **NOT NULL** by schema rules. 

#### Natural Key
An attribute of a record which can be used to uniquely identify a row but also holds real world meaning other than identification purposes (like an aadhar number)

#### Surrogate Key
An artificially generated value which solely functions to uniquely identify a row and has no real world connection outside of identification purposes.

#### Foreign Key 
The key which bridges two tables. It is borrowed from a different table. The primary key of one table can be the foreign key of multiple tables.

> Foreign keys are not Super Keys by default as they allow multiple rows under the same key, except for Foreign Keys in 1:1 Relationship Models , where the **Foreign Key is used as the Primary key or is forced to be unique**, thereby upgrading it to a candidate key.


## <u>Entity Set</u>
---
An Entity is an object of Entity Type and set of all entities is called as entity set.

- Entity set is a collection of similar entities.

- An entity set is a group of entities that passes the same set of attributes.

- Each entity in an entity set has its own set of values for the attributes which make it distinct from other entities in a table.

- No two entities in an entity set will have the same values for the attributes.

There are two types of Entity Sets.  

#### <u>Strong Entity Set</u>

- An entity set that has a primary key using which, entities in the table can be uniquely identified. This kind of entity set is termed as a strong entity set. Strong entity set is also known as a regular entity set.  
- In an ER diagram, the strong entity set is represented by the rectangle. Here, the primary key is underlined with the solid line.

**Example:** In case of Employee in class each employee is identified by unique Emp_id which is a primary key.

#### <u>Weak Entity Set</u>

A weak entity set doesn't have any primary key which can identify each entity in a set distinctly. But, for discriminating the entities in a set, the weak entity set is dependent on a particular strong entity set.

- A weak entity is also said to be existence dependent as for the existence of its entities it has to be dependent on a particular strong entity set i.e. a particular “strong entity set”.

- The relation between a weak entity set and a strong entity set is said to be identifying relationship.

- Weak entity set is represented by double rectangle.

**Example:** In case of ‘Department’ entity depend on employee entity for primary key.


## <u>Relationship</u>
---

- A relationship is used to describe the relation between entities.

- The association among entities is called a relationship.

For example, an employee works_at a department, a student enrols in a course. Here, Works_at and Enrolls are called relationships.

**Diamond or rhombus is used to represent the relationship.**

#### <u>Concepts in Relationship</u>

**Relationship Set:** A set of relationships of similar type is called a relationship set. Like entities, a relationship too can have attributes. These attributes are described attributes.

**Degree of Relationship:** The number of participating entities in a relationship defines the degree of relationship.  **2 Entities = Binary Relationship** , **3 Entities = Ternary Relationship , 4 Entities = Quaternary Relationship**

## <u>Constraints on Relationship</u>

### <u>Mapping Constraints</u>
A mapping constraint is a data constraint that expresses the number of entities to which another entity can be related via a relationship.  
It is most useful in describing the relationship sets that involve more than two entity sets.  
For binary relationship set R on an entity set A and B, there are four possible mapping cardinalities. These are as follows:  
- One to one (1:1) 
- One to many (1:M) 
- Many to one (M:1) 
- Many to many (M:M)

#### <u>One to One (1:1)</u>
In a one to one relationship, a row of a table is only related to a single row in another table.   
**Example:** Assume two tables, **StudentDetails** and **StudentAttendance** are in a 1:1 relationship with StudentID as the Foreign Key. Here, in StudentAttendance, each student with a StudentID will only have a single attendance ie a single row of data. Hence, in both the tables Student Details and Student Attendance, StudentID is the primary key used for uniquely identifying a record.

#### <u>One to Many (1:M)</u>
In a one to many relationship, a row in one table can be related to multiple rows in another table.
**Example:** Assume two tables **StudentDetails** and **Subjects** with StudentID as the Foreign Key. 

#### <u>Many to One (M:1)</u>
Multiple rows in one table are related to at most a single row in another table. It is essentially a One to Many relationship backwards.  
**Example**: In a table Subjects, A Student with the same StudentID can select multiple subjects, hence multiple rows in table Subjects are related to a single row of the corresponding StudentID in table StudentDetails.

#### <u>Many to Many (M:M)</u>
Multiple rows in one table can be related to multiple rows in another table.