Download mysql 
[majedali@majednode1 ~]$ wget http://repo.mysql.com/mysql-community-release-el6-7.noarch.rpm
Install mysql
sudo rpm -ivh mysql-community-release-el6-7.noarch.rpm
Change mysql server version
[majedali@majednode1 ~]$ sudo yum-config-manager --disable mysql56-community
[majedali@majednode1 ~]$ sudo yum-config-manager --enable mysql55-communityInstall mysql
[majedali@majednode1 ~]$ sudo yum install mysql

[majedali@majednode1 ~]$ sudo yum install mysql-server
=======================================================================================================================
 Package                             Arch                Version                   Repository                      Size
========================================================================================================================
Installing:
 mysql-community-server              x86_64              5.5.56-2.el6              mysql55-community               38 M

Transaction Summary
========================================================================================================================
Install       1 Package(s)
Mysql version
[majedali@majednode1 ~]$ mysql --version
mysql  Ver 14.14 Distrib 5.5.56, for Linux (x86_64) using readline 5.1
Download JDBC driver
[majedali@majednode1 ~]$ wget https://cdn.mysql.com//Downloads/Connector-J/mysql-connector-java-5.1.42.tar.gz
Extract JDBC driver
[majedali@majednode1 ~]$ tar zxvf mysql-connector-java-5.1.42.tar.gz	
Copy JDBC jar file
[majedali@majednode1 mysql-connector-java-5.1.42]$ sudo cp mysql-connector-java-5.1.42.jar /usr/share/java/mysql-connector-java.jar

### YUM repository

```
[majed@majednode1 ~]$ cat /etc/yum.repos.d/mysql-community.repo
[mysql-connectors-community]
name=MySQL Connectors Community
baseurl=http://repo.mysql.com/yum/mysql-connectors-community/el/6/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

[mysql-tools-community]
name=MySQL Tools Community
baseurl=http://repo.mysql.com/yum/mysql-tools-community/el/6/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

# Enable to use MySQL 5.5
[mysql55-community]
name=MySQL 5.5 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.5-community/el/6/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

# Enable to use MySQL 5.6
[mysql56-community]
name=MySQL 5.6 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.6-community/el/6/$basearch/
enabled=0
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

[mysql57-community]
name=MySQL 5.7 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.7-community/el/6/$basearch/
enabled=0
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
[majed@majednode1 ~]$
```
