# Bank Management System
 Bank management system by using Python and MySQL

Step 1: Install Python and MySQL

Step 2: Connect MySQL to Python by using Python MySQL Connector
         for install mysql python connector by using following command in CMD

          pip install mysql-connector-python

Step 3: Create database in Mysql

mysql> create database Bank_sys ; Query

mysql> create table account(Acc_no int (10) primary key, Name varchar(255), Dob varchar(10),
Address varchar(255), Mob_no int(13), Balance int(10));

mysql> create table amount(Acc_no int(10), Name varchar(255), TotalBalance int(10), foreign
key(Acc_no) references account(Acc_no));

mysql> describe account;
+------------+-------------------+------+-------+----------+-------+
| Field    | Type        | Null| Key | Default | Extra |
+------------+-------------------+------+-------+----------+-------+
| Acc_no   | int         | NO  | PRI | NULL    | |
| Name     | varchar(255)| YES |     | NULL    | |
| Dob      | varchar(10) | YES |     | NULL    | |
| Address  | varchar(255)| YES |     | NULL    | |
| Mob_no   | int         | YES |     | NULL    | |
| Balance  | int         | YES |     | NULL    | |
+------------+-------------------+------+------+----------+-------+

mysql> describe amount;
+------------------+-------------------+-------+--------+-----------+-------+ 
| Field        | Type         | Null| Key | Default | Extra |
+------------------+-------------------+-------+--------+-----------+-------+
| Acc_no       | int          | YES | MUL | NULL    | |
| Name         | varchar(255) | YES |     | NULL    | |
| TotalBalance | int          | YES |     | NULL    | |
+------------------+-------------------+-------+--------+-----------+-------+ 3 