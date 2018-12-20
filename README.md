Docker for Vtiger CRM 7.1
===

```bash
docker pull thiennq/vtiger `
```

#### Run Containers:

##### 1) MariaDB:
```bash
docker run --name mariadb -d -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=vtiger -e MYSQL_USER=vtiger_user -e MYSQL_PASSWORD=pwd --net=host mariadb
```

##### 2) Vtiger:
```bash
docker run --name vtiger -d -e DB_HOSTNAME=127.0.0.1 -e DB_USERNAME=vtiger_user -e DB_PASSWORD=pwd -e DB_NAME=vtiger -p 80:80 --net=host ruslanguns/vtiger
```

#### Docker compose:


#### TODO:
- [ ] Add docker-compose.yml
- [ ] Remove `/vtigercrm` in path
- [ ] 

#### CONFIGURATION:

Follow the steps: [http://localhost/vtigercrm](http://localhost/vtigercrm)
