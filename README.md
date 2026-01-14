# learn-sql-pt1
some sql format database


**1-Database Introduction**
RDBMS Terminology (Ringkas):

Database: Kumpulan jadual (table) yang saling berkaitan.
Table: Jadual data seperti spreadsheet.
Column: Lajur yang menyimpan jenis data yang sama.
Row: Baris data bagi satu rekod.
Redundancy: Penyimpanan data berulang untuk tingkatkan prestasi.
Primary Key: Kunci unik untuk kenal pasti satu rekod.
Foreign Key: Kunci yang menghubungkan dua jadual.
Compound Key: Kunci gabungan beberapa column.
Index: Mempercepatkan carian data.
Referential Integrity: Pastikan foreign key merujuk rekod yang wujud.

**3-Administration**
Administrative MySQL Command: 
  
USE Databasename: This will be used to select a particular database in MySQL workarea. 
SHOW DATABASES: Lists the databases that are accessible by the MySQL DBMS. 
SHOW TABLES: Shows the tables in the database once a database has been selected with the use 
command. 
SHOW COLUMNS FROM tablename: Shows the attributes, types of attributes, key information, whether 
NULL is permitted, defaults, and other information for a table. 
SHOW INDEX FROM tablename: Presents the details of all indexes on the table, including the PRIMARY KEY. 
SHOW TABLE STATUS LIKE tablename\G: Reports details of the MySQL DBMS performance and 
statistics.

**9-Data Types**
Numeric Data Types (Ringkas):

INT: Integer biasa (signed/unsigned).
TINYINT: Integer sangat kecil.
SMALLINT: Integer kecil.
MEDIUMINT: Integer sederhana.
BIGINT: Integer sangat besar.
FLOAT(M,D): Nombor perpuluhan ketepatan sederhana.
DOUBLE(M,D): Nombor perpuluhan ketepatan tinggi (REAL).
DECIMAL(M,D): Nombor perpuluhan tepat (NUMERIC).

Date and Time Types: 

DATE - A date in YYYY-MM-DD format, between 1000-01-01 and 9999-12-31. For example, December 30th, 1973 would be stored as 1973-12-30. 
DATETIME - A date and time combination in YYYY-MM-DD HH:MM:SS format, between 1000-01-01 00:00:00 and 9999-12-31 23:59:59. For example, 3:30 in the afternoon on December 30th, 1973 would be stored as 1973-12-30 15:30:00. 
TIMESTAMP - A timestamp between midnight, January 1, 1970 and sometime in 2037. This looks like the 
previous DATETIME format, only without the hyphens between numbers; 3:30 in the afternoon on December 30th, 1973 would be stored as 19731230153000 ( YYYYMMDDHHMMSS ). 
TIME - Stores the time in HH:MM:SS format. 
YEAR(M) - Stores a year in 2-digit or 4-digit format. If the length is specified as 2 (for example YEAR(2)), 
YEAR can be 1970 to 2069 (70 to 69). If the length is specified as 4, YEAR can be 1901 to 2155. The default length is 4. 

String Types: 
 
CHAR(M) - A fixed-length string between 1 and 255 characters in length (for example CHAR(5)), right padded with spaces to the specified length when stored. Defining a length is not required, but the default is 1. 
VARCHAR(M) - A variable-length string between 1 and 255 characters in length; for example VARCHAR(25). You must define a length when creating a VARCHAR field. 
BLOB or TEXT - A field with a maximum length of 65535 characters. BLOBs are "Binary Large Objects" and are used to store large amounts of binary data, such as images or other types of files. Fields defined as TEXT also hold large amounts of data; the difference between the two is that sorts and comparisons on stored data are case sensitive on BLOBs and are not case sensitive in TEXT fields. You do not specify a length with BLOB or TEXT. 
TINYBLOB or TINYTEXT - A BLOB or TEXT column with a maximum length of 255 characters. You do not specify a length with TINYBLOB or TINYTEXT. 
MEDIUMBLOB or MEDIUMTEXT - A BLOB or TEXT column with a maximum length of 16777215 characters. You do not specify a length with MEDIUMBLOB or MEDIUMTEXT. 
LONGBLOB or LONGTEXT - A BLOB or TEXT column with a maximum length of 4294967295 characters. You do not specify a length with LONGBLOB or LONGTEXT. 
ENUM - An enumeration, which is a fancy term for list. When defining an ENUM, you are creating a list of items from which the value must be selected (or it can be NULL). For example, if you wanted your field to contain "A" or "B" or "C", you would define your ENUM as ENUM ('A', 'B', 'C') and only those values (or NULL) could ever populate that field.


**10-Create Table**
Syntax:

Field Attribute NOT NULL is being used because we do not want this field to be NULL. So if user will try to create a record with NULL value, then MySQL will raise an error. 
Field Attribute AUTO_INCREMENT tells MySQL to go ahead and add the next available number to the id field. 
Keyword PRIMARY KEY is used to define a column as primary key. You can use multiple columns separated by comma to define a primary key.

