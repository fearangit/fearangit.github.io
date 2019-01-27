# 3 - Configuration

## Database configuration

ownCloud requires a database to store administrative data. For this Quickstart, we recommend using MySQL or MariaDB. You should install the ownCloud server software before installing the database. Refer to the database documentation for instructions on how to configure it.

### MySQL/MariaDB with Binary Logging Enabled

ownCloud is currently using a TRANSACTION_READ_COMMITTED transaction isolation to avoid data loss under high load scenarios. To avoid issues, you should either disable binary logging or ensure that it is correctly configured.

* Binary logging enables replication and supports backup operations, so disabling it may be a problem if these operations are required.

* To configure correctly, change the BINLOG_FORMAT = STATEMENT in the database configuration file (or the database startup script) to BINLOG_FORMAT = MIXED or BINLOG_FORMAT = ROW.

Some database configurations enforce other transaction isolation levels. To avoid data loss under high load scenarios, you need to configure the transaction isolation level accordingly. Please refer to the MySQL manual for detailed information.

### Parameters

To set up ownCloud to use any database, use the instructions in the Installation Wizard.
1. Click **Storage & database**
2. Change the data folder (if required)
3. Select **MySQL/MariaDB**
4. Enter details
5. Click **Finish setup**

You should not normally have to edit the respective values in config/config.php, but it may be required in certain circumstances.

### Configuring a MySQL or MariaDB Database

When using these databases, ensure that

* you have installed and enabled the `pdo_mysql` extension in PHP

* The **mysql.default_socket** points to the correct socket (if the database runs on the same server as ownCloud).


Now you need to create a database user and the database itself by using the MySQL command line interface. The database tables will be created by ownCloud when you log in for the first time.

To start the MySQL command line mode use:

`mysql -uroot -p`



A **mysql>** or **MariaDB [root]>** prompt will appear. Enter the following lines and confirm them with the Enter key:

    CREATE DATABASE IF NOT EXISTS owncloud;
    GRANT ALL PRIVILEGES ON owncloud.* TO 'username'@'localhost' IDENTIFIED BY 'password';

You can quit the prompt by entering:

`quit`

An ownCloud instance configured with MySQL would contain the hostname on which the database is running, a valid username and password to access it, and the name of the database. The config/config.php as created by the installation wizard would therefore contain entries like this:

      "dbtype"        => "mysql",  
      "dbname"        => "owncloud",  
      "dbuser"        => "username",  
      "dbpassword"    => "password",  
      "dbhost"        => "localhost",  
      "dbtableprefix" => "oc_",  


## External Storage Configuration

### Next, let's look at [Common Tasks](owncloud_qs_s4.html)

----
[Welcome](index.html) - [System Requirements](owncloud_qs_s1.html) - [Installation](owncloud_qs_s2.html) - [Configuration](owncloud_qs_s3.html) - [Common Tasks](owncloud_qs_s4.html) - [Connecting Clients](owncloud_qs_s5.html)
