# Домашнее задание к занятию «Система мониторинга Zabbix» - Грибова Анастасия


## Задание 1
Установите Zabbix Server с веб-интерфейсом.
#### Процесс выполнения
* Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
* Установите PostgreSQL. Для установки достаточна та версия что есть в системном репозитороии Debian 11
* Пользуясь конфигуратором комманд с официального сайта, составьте набор команд для установки последней версии Zabbix с поддержкой PostgreSQL и Apache
* Выполните все необходимые команды для установки Zabbix Server и Zabbix Web Server
#### Требования к результаты
* Прикрепите в файл README.md скриншот авторизации в админке
* Приложите в файл README.md текст использованных команд в GitHub

![Название скриншота 1](https://github.com/gribova-anastasia/zabbix-8-03/blob/b1a216638adf7d4862495479226461e59f02ea40/adminka.png)

* sudo apt install postgresql
* wget https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1+debian11_all.deb
* dpkg -i zabbix-release_6.4-1+debian11_all.deb
* apt update
* apt install zabbix-server-pgsql zabbix-frontend-php php7.4-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent
* sudo -u postgres createuser --pwprompt zabbix
* sudo -u postgres createdb -O zabbix zabbix
* zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix
* sudo nano /etc/zabbix/zabbix_server.conf
* systemctl restart zabbix-server zabbix-agent apache2
* systemctl enable zabbix-server zabbix-agent apache2

## Задание 2
Установите Zabbix Agent на два хоста.
#### Процесс выполнения
* Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
* Установите Zabbix Agent на 2 виртмашины, одной из них может быть ваш Zabbix Server
* Добавьте Zabbix Server в список разрешенных серверов ваших Zabbix Agentов
* Добавьте Zabbix Agentов в раздел Configuration > Hosts вашего Zabbix Servera
* Проверьте что в разделе Latest Data начали появляться данные с добавленных агентов
#### Требования к результаты
* Приложите в файл README.md скриншот раздела Configuration > Hosts, где видно, что агенты подключены к серверу
* Приложите в файл README.md скриншот лога zabbix agent, где видно, что он работает с сервером
* Приложите в файл README.md скриншот раздела Monitoring > Latest data для обоих хостов, где видны поступающие от агентов данные.
* Приложите в файл README.md текст использованных команд в GitHub
![Название скриншота 1](https://github.com/gribova-anastasia/zabbix-8-03/blob/c61419a59634e71516c9fda94057a341826c94f8/config-hosts.png)

!![Название скриншота 2](https://github.com/gribova-anastasia/zabbix-8-03/blob/2c2e2da3ce8f292e3cf62bd1e19007ec2d10557c/log_agent.png)
!!![Название скриншота 2](https://github.com/gribova-anastasia/zabbix-8-03/blob/2c2e2da3ce8f292e3cf62bd1e19007ec2d10557c/log_agent.png)`

###### на хостах был установлен агент:
* wget https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1+debian11_all.deb
* dpkg -i zabbix-release_6.4-1+debian11_all.deb
* apt update
* apt install zabbix-agent
* systemctl restart zabbix-agent
* systemctl enable zabbix-agent
* sudo nano o /etc/zabbix/zabbix_agentd.conf
* sudo systemctl restart zabbix-agent
