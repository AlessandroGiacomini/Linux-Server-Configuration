## Project: Linux Server Configuration - Alessandro Giacomini
### Description
-----------------------------------
I configured a secured remote virtual machine to host a databse server, and web appllications which are data driven. This was accomlished through a provided Linux distribution by [Udacity](https://www.udacity.com), and an installed Apache2 server to serve Python Flask application that connects to PostgresSQL database.

The project deploys [tripNet App](https://github.com/AlessandroGiacomini/tripNet) on the virtual machine
It is reacheable under the AWS - server at ec2-54-70-175-224.us-west-2.compute.amazonaws.com

**Note** : The result is reached but if you are viewing this page, and trying to access the website via the IP links, the website might be off the live server

### Project Access
-----------------------------------
##### IP address

**`54.70.175.224`**

##### SSH Port

**`2200`**

##### Web Application URL

http://54.70.175.224/ 

* AWS-Server: 
http://ec2-54-70-175-224.us-west-2.compute.amazonaws.com
 
### Installed Packages
-----------------------------------
Package Name | Description
--------------: | :------------
**finger:** | Displays an easy to read information about a user
**apache2** | HTTP Server
**libapache2-mod-wsgi** | hosts Python applications on Apache2 server
**ntp** | Synchronizes time over a network
**postgresql** | Postgresql Database server
**git** | Version control system tools
**python-setuptools** | An easy-install package to facilitate installing Python packages
**sqlalchemy** | ORM and SQL tools for Python
**flask** | Microframework for web applications
**python-psycopg2** | PostgreSQL adapter for Python
**oauth2** | Authorization framework for third-party login (Google and Facebook)
**google-api-python-client** | Google API for OAuth login
**Glances** | Application monitor for host bugs

### Configuration Summary
-----------------------------------
- Setup Virtual Machine and SSH into the server.
- A new system user `grader` was created with permission to sudo.
- All cuurently installed packages were updated and upgraded.
- CRON tasks added to `update` and `upgrade` installed packages.
- Changed SSH Port from `22` to `2200` and configure SSH access.
- Configured `UFW`to only allow incoming connections for `SSH(Port:2200)`, `HTTP(Port:80)` and `NTP(Port:123)`.
- Configured local Time Zone to `UTC`.
- Installed and configure `Apache` to serve a `Python mod_wsgi` application.
- Installed Git and Setup Environment for delopying Flask Application.
- Install and configure `PostgreSQL` with default settings to *not* allow remote connection.
- Created a new user `catalog`, added user to PostgreSQL databse with limited permissions to catalog application database.
- Get OAUTH-LOGINS (Google+ and Facebook) working.