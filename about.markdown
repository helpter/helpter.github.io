---
layout: page
title: About
permalink: /about/
---

This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](https://jekyllrb.com/)

You can find the source code for Minima at GitHub:
[jekyll][jekyll-organization] /
[minima](https://github.com/jekyll/minima)

You can find the source code for Jekyll at GitHub:
[jekyll][jekyll-organization] /
[jekyll](https://github.com/jekyll/jekyll)


[jekyll-organization]: https://github.com/jekyll




1. Our server system is the CentOS 7.2 64-bit, do not have to CentOS system, please search the installation method for other systems.
2. Installing nginx
3. To set up the yum repository for RHEL/CentOS, create the file named /etc/yum.repos.d/nginx.repo with the following contents:

\[nginx\]

name=nginx repo

baseurl=<http://nginx.org/packages/mainline/centos/7/$basearch/>

gpgcheck=0

enabled=1

1. Update Yum,then run the following command:

yum update

1. Check the version of nginx, whether it is consistent with the official version then run the following command:

yum list nginx

1. Install nginx

yum install -y nginx

1. Nginx has been installed, you can start the service and visit you server IP to test. Please use the nginx.conf file to configure the domain name or root path.

Nginx service management.

# start service

service nginx start

# stop service

service nginx stop

# restart service

service nginx restart

1. Installing Mysql
2. Download the rpm file then run the following command:

wget <http://dev.mysql.com/get/mysql57-community-release-el7-7.noarch.rpm>

1. Install rpm

rpm -ivh <http://dev.mysql.com/get/mysql57-community-release-el7-7.noarch.rpm>

1. Update Yum

yum update

1. Install mysql

yum install -y mysql-community-server

1. Start mysql service

service mysqld start

1. Get the default password for mysql

grep ‘temporary password’ /var/log/mysqld.log

```
2015-11-30T03:16:23.337689Z 1[Note] A temporary password is generated  
for root@localhost y!W?D_q+16lp
```
![](data:image/png;base64,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)

After running the command you will get a string like this, and ‘ylW?D-q+l6lp’is the password.

1. Mysql safe configuration. Run the following command:

mysql_secure_installation

1. You can log in with the following command, and the password is what you just set.

mysql -u root -p

1. Installing mosquitto (MQTT)
2. Create the file named /etc/yum.repos.d/mosquitto.repo with the following contents:

\[home_oojah_mqtt\]

name=mqtt (CentOS_CentOS-7)

type=rpm-md

baseurl=<http://download.opensuse.org/repositories/home:/oojah:/mqtt/CentOS_CentOS-7/>

gpgcheck=1

gpgkey=<http://download.opensuse.org/repositories/home:/oojah:/mqtt/CentOS_CentOS-7/repodata/repomd.xml.key>

enabled=1

1. Update Yum

yum update

1. Install mosquitto with the following commands:

yum search all mosquitto

yum install mosquitto mosquitto-clients

1. Start mosquitto service

service mosquitto start

1. Installing influxdb
2. Run the following commands

wget <https://dl.influxdata.com/influxdb/releases/influxdb-1.0.2.x86_64.rpm>

yum localinstall influxdb-1.0.2.x86_64.rpm

1. Start influxdb service

service influxdb start

1. Installing java
2. Download jdk8 64-bit, the link:

<http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html>

tar -zxvf jdk-8u91-linux-x64.tar.gz
```bash
[root@localhost dev]# pwd
/usr/dev
[root@localhost dev]# ls
jdk1.8.0_91
[root@localhost dev]# 
```


1. Configure environment variables  
For example: Edit the file with the following command:  
vi /etc/profile  
Add the following content at the bottom of the file:  
JAVA_HOME=/usr/dev/jdk1.8.0_91  
PATH=$JAVA_HOME/bin:$PATH  
CLASSPATH=$JAVA_HOME/jre/lib/ext:$JAVA_HOME/lib/tools.jar  
export PATH JAVA_HOME CLASSPATH  
Run the following command to take effect.  
source /etc/profile  
Run the following command to test whether installed successfully.  
java -version

1. Configuration
2. You need to confirm whether all the above stuff are started;
3. Use the editor to open the public folder, the global search for the contents of ‘iot.beaconyun.com’, replace it with your IP address or domain name. And then copy all the documents under the public to root directory by nginx.conf, visit IP or domain name can open on the line;
4. Configure the mysql database, build user and give the password.

mysql -u root -p

create user ‘by_iot’@’localhost’ identified by ‘password’;

Authorization

grant all on \*.\* to ‘by_iot’@’localhost’;

flush privileges

Create database ‘by_iot’

Create database by_iot;

Import the database table structure into the database, exit mysql then run the following command:

mysql -u root -p by_iot < by_iot.sql

1. Configure the influxdb database, build database‘test’ with the following commands:

influx

create database test;

create retention policy by_iot on test duration 30d replication 1 default;

1. Copy thingoo-server-1.1.7.jar to a directory on your server then run the following command:

java -jar thingoo-server-1.1.7.jar

If you want this java command has been always running, you should install screen.

1. Open the your IP address or domain name which you configured with nginx.conf. Register , log in then view the data. You can know more from the file Thingoo G1 BeaconYun IoT Service Dashboard User Guide.docx

Note：

1.Mysql turned on SSL but not configured, but the jdbc configuration url added ‘useSSL = true’, it will be an error. So you can remove useSSL or close SSL, add ‘skip_ssl’ statement in the my.cnf file of Mysql, then restart the database.

2.You need to open port 8080,3306, 8083 of the firewall.

File description：

iot-frontend Front source code

public The static files built by front source code

thingoo-server Backend source code

thingoo-server-1.1.7.jar The .jar packaged by backend source code

by_iot.sql The table structure of database

Above you have to build a good deployment environment, then the following is to build a development environment.

1、How to run the front source code on your local machine？

Firstly, you need to install tools.

- Download and install git
- Download and install nodejs <https://nodejs.org>

My local machine installed node.js v6.11.1, npm v3.10.10. Then go inside of iot-frontend directory, and open a cmd window, run the following commands:

Install dependencies

npm install -g bower

npm install -g gulp

bower install

npm install

Run

gulp serve

Build

gulp build

1. How to package by backend source code on your local machine?

Firstly, you need to install maven 3.5.0. Then go inside of thingoo-server directory, and open a cmd window, run the following command:

mvn package

If successful, you will find .jar file in the target folder.