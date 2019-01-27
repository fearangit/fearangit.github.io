# 1 - System Requirements and Deployment Recommendations

Before we start, let's make sure that your system is capable of running ownCloud.


### Operating System
You can run ownCloud on any of the following Linux systems. The enterprise versions are ideal for large-scale deployments, but for the purposes of this Quickstart installation, Ubuntu is ideal as it comes with the full set of required packages out of the box.
- Ubuntu 16.04 and 18.04
- Debian 7 and 8
- Red Hat Enterprise Linux 6 and 7
- Centos Linux 6 and 7
- Fedora 27 and 28
- SUSE Linux Enterprise Server 12 with SP1, SP2 and SP3
- openSUSE Tumbleweed and Leap 15.0, 42.3


### Database
Any of the listed databases can be used, but MySQL or MariaDB are recommended for this Quickstart installation.
- MySQL or MariaDB 5.5+ (with InnoDB storage engine)
- Oracle 11g
- PostgreSQL
- SQLite

### Web Server
Apache 2.4 with prefork Multi-Processing Module (MPM) and mod_php

### PHP Runtime
5.6, 7.0, 7.1 or 7.2

### Memory Requirements
Memory requirements vary greatly, depending on the numbers of users and files, and the volume of server activity. The official minimum recommandation is 128 MB RAM. However, we strongly recommend a minimum of 512 MB to ensure reasonable performance.

### Command line access
ownCloud administrators should use hosts that provide command-line and Cron access.
- OCC commands, required for administrative tasks such as repairs and upgrades, are only available using the command line.
- You need crontab access to run background jobs reliably. 

## Deployment recommendations
Both ownCloud and the LAMP stack are highly configurable. An ownCloud installation can range from a single machine hosting the application, assocated LAMP stack and local storage, up to enterprise-level systems with multiple applications, databases and web servers providing file sharing to tens of thousands of users. This Quickstart describes the simplest type of installation, which will enable you to get started and learn the basics of ownCloud.

Once you are up and running, you will see that the server load is dependent on the number of clients, files, and patterns of user activity. Once you are confident that your ownCloud installation is running smoothly, the next step then is to scale up the system to provide the service to a small workgroup or department.

### Workgroup scenario
This scenario applies where you have up to 150 users, 100 GB to 10 TB of storage, and you make provision for High Availability.
The recommended system is to have a single physical server running the application, web, and database server, as well as local storage. You can provide authentication through an existing LDAP or Active Directory server.

The physical server should have at least two CPU cores, 16 GB of RAM, and sufficient local storage as needed. Remember that the amount of data stored in ownCloud will only grow, so ensure that you can easily increase the storage capacity when required.

For the operating system, we recommend an enterprise-grade Linux distribution with full support from the vendor. Red Hat Enterprise Linux is an excellent choice for OS in this scenario.

For the database, MySQL or MariaDB are both suitable, just make sure they are using the InnoDB storage engine.

For backup, install ownCloud, the ownCloud data directory, and database on a [Btrfs](https://en.wikipedia.org/wiki/Btrfs) filesystem. Make regular snapshots at desired intervals for zero downtime backups. Mount DB partitions with the `nodatacow` option to prevent fragmentation. Alternatively, you can make nightly backups, but these will entail some service interruption.


### Larger scenarios
For details of implementing larger ownCloud deployments, go to the [Deployment Recommendations](https://doc.owncloud.org/server/10.0/admin_manual/installation/deployment_recommendations.html) section of the Admin Guide. This describes two further scenarios, **mid-sized enterprises** (from 150 to 1,000 users) and **large enterprises and service providers** (5,000 to 100,000 users).








----
[Welcome](index.html) | System Requirements | [Installation](owncloud_qs_s2.html) | [Configuration](owncloud_qs_s3.html) | [Common Tasks](owncloud_qs_s4.html) | [Connecting Clients](owncloud_qs_s5.html)
