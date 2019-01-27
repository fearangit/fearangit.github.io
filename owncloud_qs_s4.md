# 4 - Common Administrative Tasks
You can do...

## Setting Server IP Address and Port

ownCloud uses the config/config.php file to control server operations. Most options are configurable on your Admin page, so it is usually not necessary to edit config/config.php.

The default parameters are configured by the ownCloud installer, and are required for your ownCloud server to operate.

The `'dbhost' => '',` parameter is one of these default parameters configured by the ownCloud installer. This parameter specifies your host server name, for example _localhost_, _hostname_, or the IP address. To specify that Port 8080 should be used, set it as follows:

> 'dbhost' => 'hostname:8080'


## Creating a New User

To create a new user account:

1. Go to the User management page of your ownCloud Web UI
2. Enter the new user’s **Login Name** and their initial **Password**
3. Assign **Groups** memberships (this is optional)
4. Click the **Create** button

Login names may contain letters (a-z, A-Z), numbers (0-9), dashes, underscores, periods, and the 'at' sign (@). After creating the user, you may fill in their full name if it is different than the login name, or leave it for the user to complete.

If you have checked **Send email to new user** in the control panel on the lower left sidebar, you may also enter the new user’s email address, and ownCloud will automatically send them a notification with their new login information. You may edit this email using the email template editor on your Admin page.

### Next, let's look at [Connecting Clients](owncloud_qs_s5.html)

----
[Welcome](index.html) - [System Requirements](owncloud_qs_s1.html) - [Installation](owncloud_qs_s2.html) - [Configuration](owncloud_qs_s3.html) - [Common Tasks](owncloud_qs_s4.html) - [Connecting Clients](owncloud_qs_s5.html)
