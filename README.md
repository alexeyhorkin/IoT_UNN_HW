# IoT_UNN_HW

Все необходимые данные находятся в скрытых директорях `.mytb-data`, `.mytb-logs`, `.node-red-data`. Все эти директории являются volumes для контейнеров `node-red` и `thingsboard`.

## Запуск
---
### Linux only

```console
sudo chown -R 799:799 .mytb-data
sudo chown -R 799:799 .mytb-logs
```
На мак эти действия выполнять не нужно

---
### Main command
Из текущего репозитория:
```console
docker-compose up
```


> Заметьте, что скорее всего в вашем случае контейнер `thingsboard` упадет с ошибкой, по стрек трейсу которого можно понять, что проблема с подключением к базе данных.
На самом деле, вам нужно просто подождать)

Скорее всего миграция базы данных postgres занимает некоторое длительное время, но код java внутри контейнера этого не предусматривает (как жаль)

## Links:
* [thingsboard](http://localhost:8080/)
* [node-red](http://localhost:1880/)

## Credentials:
* System Administrator: sysadmin@thingsboard.org / sysadmin
* Tenant Administrator: tenant@thingsboard.org / tenant
* Customer User: customer@thingsboard.org / customer
