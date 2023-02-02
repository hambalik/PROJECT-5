##  **PROJECT 5 - CLIENT - SERVER ARCHITECTURE WITH MYSQL**

## STEP 1 – CREATION OF CLIENT AND DATABASE SERVER INSTANCES


### DB-server and client instances created

![instances-creation](./images/instances-creation.PNG)


## STEP 2 – MYSQL-SERVER INSTALLATIONS

### mysql-server installation on DB-server

`sudo apt update -y`
`sudo apt install mysql-server -y`

![mysql-server-installation](./images/sudo-apt-update.PNG)
![mysql-server-installation](./images/mysql-server-installation.PNG)
![mysql-server-installation1](./images/mysql-server-installation1.PNG)
![mysql-server-installation2](./images/mysql-server-installation2.PNG)
![mysql-server-installation3](./images/mysql-server-installation3.PNG)
![mysql-server-installation4](./images/mysql-server-installation4.PNG)


### Enabling mysql service

`sudo systemctl enable mysql`

![enabling-the-system](./images/enabling-the-system.PNG)

## STEP 3 – CLIENT INSTALLATIONS

### Cient instance updated

`sudo apt update`

![sudo-apt-update-client](./images/sudo-apt-update-client.PNG)

### Installation of mysql-installation

`sudo apt install mysql-client -y`

![install-mysql-client](./images/install-mysql-client.PNG)

## STEP 4 – SECURITY GROUP TO RESTRICT REMOTE ACCESS TO ONLY CLIENT

### Security group edited

![server-sec-edit](./images/server-sec-edit.PNG)

### Security scrip running on mysql-server

`sudo mysql_secure_installation`

![mysql-secure-instalation](./images/mysql-secure-instalation.PNG)

### running mysql

`sudo mysql`

![database-creation-on-mysql1](./images/database-creation-on-mysql1.PNG)

### configuration of mysql-server to allow connections from remote hosts

`sudo vi /etc/mysql.conf.d/mysqld.cnf`

![bind-address1](./images/bind-address1.PNG)

![bind-address](./images/bind-address.PNG)

### restarting the service

`sudo systemctl restart mysql`

![restart-mysql](./images/restart-mysql.PNG)

### conneting remotely to mysql server datbase engine from client using mysql utility

`sudo mmysql -u remote_user -h 172.31.81.122 -p`

![client-mysql](./images/client-mysql.PNG)

### Lastly, confirm that you have successfully connected to a remote MYSQL server

`show databases`

![show-database-from-client1](./images/show-database-from-client1.PNG)

