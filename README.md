# mysql-server-error

## Error -1)
ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/var/run/mysqld/mysqld.sock' (2)
Resolve this error by using these command :

### Uninstalling mysql server ---

``` $ sudo apt autoremove --purge mysql-server\* mariadb-server\*  ```

![image](https://user-images.githubusercontent.com/116658648/211995692-e5412133-135b-42fe-814d-54e6a3d59d52.png)

![image](https://user-images.githubusercontent.com/116658648/211995767-499149aa-384f-4cec-8857-3e58b8a16918.png)

### Installing mysql server ---

```
$ sudo rm -rf /var/lib/mysql
$ sudo rm -rf /etc/mysql/
$ sudo mkdir -p /etc/mysql/conf.d
$ sudo apt install mysql-server
```

![image](https://user-images.githubusercontent.com/116658648/211996113-1a323b48-ddf6-4658-8cbe-70358b50b95b.png)

![image](https://user-images.githubusercontent.com/116658648/211997109-d214a2b0-ca63-4f26-b10e-3cd907a73635.png)

```
sudo service mysql status

```
![image](https://user-images.githubusercontent.com/116658648/211996944-d8a6dbb9-61f1-4392-81f5-4dcc4fbb8d24.png)

## Error -2)
ERROR 1698 (28000): Access denied for user 'root'@'localhost'


``` mysql -u root -p ```

![image](https://user-images.githubusercontent.com/116658648/211997826-f64841c4-c6eb-4afe-a362-f5c8b1951be2.png)

``` sudo mysql ```

![image](https://user-images.githubusercontent.com/116658648/211998680-0fdfa34d-d3d1-42d9-8104-628a2b93bee8.png)

Change Current-Root-Password to your root password 

``` ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Current-Root-Password'; ```

``` FLUSH PRIVILEGES; ```

![image](https://user-images.githubusercontent.com/116658648/211998680-0fdfa34d-d3d1-42d9-8104-628a2b93bee8.png)








 

