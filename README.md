<p align="center"> Ansible Role for installing and configuring mysql
    <br> 
</p>


### Role Variables

| Variable Name | Value | Type | Default |
| ------ | ------ | ------ | ------ |
| mysql_version | defines which version of mysql will be installed | String | 8.0 |
| mysql_root_password | defines the password of root user | String | ScandiwebTest1234! |
| mysql_users | defines users to be created | List of Dictionaries | None |
| mysql_databases | defines databases to be created | List | None |



`Example:`
```
---
mysql_root_password: Test!scandiweb1234

mysql_databases:
  - magento_scandiweb

mysql_users:
  - name: magento_scandiweb
    host: "localhost"
    password: "scandiweb"
    priv: "magento_scandiweb.*:ALL"
```