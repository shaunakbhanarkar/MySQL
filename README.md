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

