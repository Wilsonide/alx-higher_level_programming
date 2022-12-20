#  0x0D. SQL - Introduction

## Database Installation and Commands on UBUNTU 20.4

### Installation

* Install MySQL Server
    - $ ```sudo apt install mysql-server```

### Setup and Commands

1. Set password for the first time
    - $ ```mysqladmin -u root password NEWPASSWORD```

2. Change existing Password
    - $ ```sudo mysql ALTER USER 'root'@'localhost' IDENTIFIED BY 'PASSWORD';```
    - $ ```sudo systemctl stop mysql```
    - $ ```sudo mysqld -init-file=~/mysql-pwd```
    - $ ```sudo systemctl start mysql```

3. Import dumb table into a database
    - $ ```mysql -u root -p 'database_name' < 'filename.sql'```

4. Download file online
    - $ ```wget 'https://web_address.com'/filename```

5. Enter mysql prompt
    - $ ```mysql -u root -p```

6. Create New MySQL User
    - mysql> ```CREATE USER 'username'@'host' IDENTIFIED WITH authentication_plugin BY 'password';```

7. Create New MySQL User with mysql_native_password
    - mysql> ```CREATE USER 'sammy'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';```

8. Alter MySQL User with mysql_native_password
    - mysql> ```ALTER USER 'sammy'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';```

9. Granting a User Permissions
    - mysql> ```GRANT PRIVILEGE ON database.table TO 'username'@'host';```
    - mysql> ```GRANT CREATE, ALTER, DROP, INSERT, UPDATE, DELETE, SELECT, REFERENCES, RELOAD on *.* TO 'sammy'@'localhost' WITH GRANT OPTION;```

10. Granting All privileges to a User
    - mysql> ```GRANT ALL PRIVILEGES ON *.* TO 'sammy'@'localhost' WITH GRANT OPTION;```

11. Reload grant table to effect new privileges
    - mysql> ```FLUSH PRIVILEGES;```

12. Revoke a permission
    - mysql> ```REVOKE type_of_permission ON database_name.table_name FROM 'username'@'host';```

13. Review a User permissions
    - mysql> ``````SHOW GRANTS FOR 'username'@'host';```

14. Delete a User
    - mysql> ```DROP USER 'username'@'localhost';```

15. Exit MySQL clint
    - mysql> ```exit```

16. New User log in
    - $ ```mysql -u username -p```

### Usage
 
* Usage Example: $ ```cat 0-list_databases.sql | mysql -uroot -p```

### Resources

* (What is Database & SQL?)
