Docker for Vtiger CRM 7.1
===

```bash
docker pull thiennq/vtiger `
```

### Run Containers:

##### 1) MariaDB:
```bash
docker run --name mariadb -dit \
-e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=vtiger -e MYSQL_USER=vtiger_user -e MYSQL_PASSWORD=pwd \
--net=host mariadb
```

##### 2) Vtiger:
```bash
docker run --name vtiger -dit \
-e DB_HOSTNAME=127.0.0.1 -e DB_USERNAME=vtiger_user -e DB_PASSWORD=pwd -e DB_NAME=vtiger \
-p 80:80 --net=host ruslanguns/vtiger
```

### Docker compose:
- Update environment variables
- Run
```bash
docker-compose up -d
```


### CONFIGURATION:
Follow the steps: [http://localhost](http://localhost)
