## 1 - System Requirements and Deployment Recommendations

Before we start, let's make sure that your system is capable of running ownCloud.


### OS
You can run ownCloud on any of the following Linux systems. The enterprise versions are ideal for large scale deployments, but for the purposes of this Quickstart, we recommend Ubuntu, as it comes with the full set of required packages out of the box.
- Ubuntu 16.04 and 18.04
- Debian 7 and 8
- Red Hat Enterprise Linux 6 and 7
- Centos Linux 6 and 7
- Fedora 27 and 28
- SUSE Linux Enterprise Server 12 with SP1, SP2 and SP3
- openSUSE Tumbleweed and Leap 15.0, 42.3


### DB
MySQL or MariaDB are ideal for this Quickstart.
- MySQL or MariaDB 5.5+
- Oracle 11g
- PostgreSQL
- SQLite

### Web Server
Apache 2.4 with prefork Multi-Processing Module (MPM) and mod_php

### PHP Runtime
5.6, 7.0, 7.1 or 7.2

### Memory Requirements
Memory requirements vary greatly, depending on the numbers of users and files, and the volume of server activity. The official minimum recommandation is 128MB RAM. However, we strongly recommend a minimum of 512MB to ensure reasonable performance.



## Deployment recommendations
General
Scale out , cloud sharing, amount of data will grow, so plan ahead

## Command line access
ownCloud administrators should use hosts that provide command-line and Cron access.
- OCC commands, required for administrative tasks such as repairs and upgrades, are only available using the command line.
- You need crontab access to run background jobs reliably. 


Small Workgroup/dept

Deployment considerations
Single machine - scale up, or scale out with cluster


----
[Welcome](index.html) | System Requirements | [Installation](owncloud_qs_s2.html) | [Configuration](owncloud_qs_s3.html) | [Common Tasks](owncloud_qs_s4.html) | [Connecting Clients](owncloud_qs_s5.html)
