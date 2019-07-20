# MySQL

You are supposed to check whether you have the ‘bank’ Database set-up on your local machines. If you do so then drop the database, and create a new database with the same name and use it.

mysql> create database bank;

mysql> use bank;

Once you’ve done this, download the bank.sql file (available on moodle) to your home directory. Then execute the folowing command in your terminal.

mysql> source bank.sql

 show tables;
+----------------+
| Tables_in_bank |
+----------------+
| ACCOUNT        |
| ASSETS         |
| BORROWER       |
| BRANCH         |
| CUSTOMER       |
| DEPOSITOR      |
| LOAN           |
| PAYMENT        |
+----------------+
8 rows in set (0.00 sec)

mysql> desc account;
+---------+---------------+------+-----+---------+-------+
| Field   | Type          | Null | Key | Default | Extra |
+---------+---------------+------+-----+---------+-------+
| ACC_NO  | varchar(20)   | NO   | PRI |         |       |
| BALANCE | decimal(10,0) | YES  |     | NULL    |       |
| BR_NAME | varchar(20)   | NO   | MUL | NULL    |       |
+---------+---------------+------+-----+---------+-------+
3 rows in set (0.01 sec)

mysql> desc assets;
+------------+-------------+------+-----+---------+-------+
| Field      | Type        | Null | Key | Default | Extra |
+------------+-------------+------+-----+---------+-------+
| BR_NAME    | varchar(10) | NO   | PRI |         |       |
| FACILITIES | varchar(20) | NO   | PRI |         |       |
+------------+-------------+------+-----+---------+-------+
2 rows in set (0.00 sec)

mysql> desc borrower;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| CUST_ID | char(5)     | NO   | MUL | NULL    |       |
| LOAN_NO | varchar(30) | NO   | MUL | NULL    |       |
+---------+-------------+------+-----+---------+-------+
2 rows in set (0.00 sec)

mysql> desc branch;
+----------+-------------+------+-----+---------+-------+
| Field    | Type        | Null | Key | Default | Extra |
+----------+-------------+------+-----+---------+-------+
| BRN_NAME | varchar(10) | NO   | PRI | NULL    |       |
| CITY     | varchar(30) | YES  |     | NULL    |       |
+----------+-------------+------+-----+---------+-------+
2 rows in set (0.00 sec)

mysql> desc customer;
+--------+-----------------------+------+-----+---------+-------+
| Field  | Type                  | Null | Key | Default | Extra |
+--------+-----------------------+------+-----+---------+-------+
| C_ID   | char(5)               | NO   | PRI | NULL    |       |
| NAME   | varchar(30)           | YES  |     | NULL    |       |
| STREET | varchar(25)           | YES  |     | NULL    |       |
| CITY   | varchar(30)           | YES  |     | NULL    |       |
| GENDER | enum('f','F','m','M') | YES  |     | NULL    |       |
+--------+-----------------------+------+-----+---------+-------+
5 rows in set (0.00 sec)

mysql> desc depositor;
+-----------+-------------+------+-----+---------+-------+
| Field     | Type        | Null | Key | Default | Extra |
+-----------+-------------+------+-----+---------+-------+
| CUST_ID   | char(5)     | NO   | MUL | NULL    |       |
| AC_NO     | varchar(20) | YES  |     | NULL    |       |
| ACCESS_DT | date        | YES  |     | NULL    |       |
+-----------+-------------+------+-----+---------+-------+
3 rows in set (0.00 sec)

mysql> desc loan;
+---------+---------------+------+-----+---------+-------+
| Field   | Type          | Null | Key | Default | Extra |
+---------+---------------+------+-----+---------+-------+
| LN_NO   | char(10)      | NO   | PRI | NULL    |       |
| AMOUNT  | decimal(10,0) | YES  |     | NULL    |       |
| BR_NAME | varchar(10)   | YES  | MUL | NULL    |       |
+---------+---------------+------+-----+---------+-------+
3 rows in set (0.01 sec)

mysql> desc payment;
+--------+---------------+------+-----+---------+-------+
| Field  | Type          | Null | Key | Default | Extra |
+--------+---------------+------+-----+---------+-------+
| P_NO   | varchar(10)   | NO   | PRI |         |       |
| L_NO   | varchar(20)   | NO   | PRI |         |       |
| DATE   | date          | YES  |     | NULL    |       |
| AMOUNT | decimal(10,0) | YES  |     | NULL    |       |
+--------+---------------+------+-----+---------+-------+
4 rows in set (0.00 sec)

