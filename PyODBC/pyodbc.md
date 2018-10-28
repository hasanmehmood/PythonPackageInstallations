Inorder to install PyODBC, You need to install ODBC driver first.

```
sudo su 
curl https://packages.microsoft.com/keys/microsoft.asc | apt-key add -
```

-Download appropriate package for the OS version
-Choose only ONE of the following, corresponding to your OS version

**Ubuntu 14.04**

`curl https://packages.microsoft.com/config/ubuntu/14.04/prod.list > /etc/apt/sources.list.d/mssql-release.list`

**Ubuntu 16.04**

`curl https://packages.microsoft.com/config/ubuntu/16.04/prod.list > /etc/apt/sources.list.d/mssql-release.list
`

**Ubuntu 17.10**

`curl https://packages.microsoft.com/config/ubuntu/17.10/prod.list > /etc/apt/sources.list.d/mssql-release.list`

**Ubuntu 18.04**

`curl https://packages.microsoft.com/config/ubuntu/18.04/prod.list > /etc/apt/sources.list.d/mssql-release.list`


```
exit
sudo apt-get update
sudo ACCEPT_EULA=Y apt-get install msodbcsql17

```
**optional: for bcp and sqlcmd**
```
sudo ACCEPT_EULA=Y apt-get install mssql-tools
echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bash_profile
echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bashrc
source ~/.bashrc

```
**optional: for unixODBC development headers**
`sudo apt-get install unixodbc-dev`

**Now install PyODBC**
`pip install pyodbc`

**For More Information Please follow below link.**
<https://docs.microsoft.com/en-us/sql/connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server?view=sql-server-2017>

