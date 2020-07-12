# Database Management System  
  
*Written by Jiayue Wu, Youhui Yang, Ting Zuo*  
  
This is a basic database management system. Run in terminal. Start from src/execute/main.java. src/execute/execute.java is used to create data file used to test.  
  
## Structure:  
  
Attribute: Name, type, primary key, foreign key, tuple list  
Primary key not allow duplicates;  
Foreign key not allow value not in reference attribute;  
Tuples are saved in ArrayList. Types allowed: Integer, Double, Character, String.  
  
Table: Name, attribute list, table directory, dictionary directory, database name, attribute set  
Attributes saved in ArrayList;  
Table are saved in .csv;  
Dictionary is used to save attribute information;  
Attribute set is a hashset used to check whether an attribute exists or get the number of attributes;  
Enable to save table to .csv file, and load .csv file.  
  
Sql:  
Create - used to create table file and dict file;  
Update - used to update tuples in table, one time one condition;  
Insert - used to insert data into table, one time one line;  
Delete - used to remove target tuples;  
Drop - used to drop table, delete the table file and dict file;  
Select - overwrite, can choose from select * or select attribute(s), display the result;  
Where - add some conditions to select. Allowed conditions include: >, <, =, !=, >=, <=, work as join.  
Where_index - use index to find the target attribute.  
Order by - select table, display it in asc or desc order of one target attribute.  
Group by - together with functions. Functions include avg(), sum(), min(), max(), count(). Display the group by attribute and the function result. One time one group by attribute and one function.  
Having - after group by.  

  

## Optimization:  
  
We enable the index on single attribute; (done)  
The selection at bottom; (done)  
Able to choose merge join or nested_join according to the tables’ sizes; (done)  
Able to determine the outer layer and inner layer table for nested_join according to the tables’ size; (done)  
Able to Sort the conditions according to the corresponding attribute’s selectivity; (done)  
The projection at bottom; (not done)  

  
## Query Input Manager:  
  
The program implemented below listed functions for Query Input Manager.  
Input  
Input queries with command line editor  
Exit program by inputting “quit;”  
Recursive input queries and each query end with “;”  
Wrong query grammar detection with error message display  
Parser  
Obtain input SQL queries and divide into multiple sections for further processing  
Data Definition Language  
CREATE / DROP TABLE  
CREATE / DROP INDEX   
Data Manipulation Language  
SELECT  
INSERT INTO  
INSERT…SELECT  
UPDATE  
DELETE  


