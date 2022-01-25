# IoT_UNN_HW

Репозиторий для сдачи домашнего задания по курсу "Интернет вещей" 2021.

Все необходимые данные для `thingsboard` находятся в скрытых директорях `.mytb-data`, `.mytb-logs`, данные для `node-red` находятся в `.node-red-data`. Все эти директории являются volumes для контейнеров.

## Запуск
---
### Linux
```console
mkdir .mytb-logs
sudo chown -R 799:799 .mytb-data
sudo chown -R 799:799 .mytb-logs
```
### Mac-OS
На Mac-OS эти действия выполнять не нужно, работает out-of-the-box.

### Windows
Не тестировалось, скорее всего не работает =)

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
* Tenant Administrator: tenant@thingsboard.org / tenant [мы используем эту учётную запись ✔️]
* Customer User: customer@thingsboard.org / customer
