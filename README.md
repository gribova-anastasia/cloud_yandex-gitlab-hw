# Домашнее задание к занятию «Система мониторинга Prometheus» - Грибова Анастасия


## Задание 1
Установите Prometheus.
#### Процесс выполнения
* Выполняя задание, сверяйтесь с процессом, отражённым в записи лекции
* Создайте пользователя prometheus
* Скачайте prometheus и в соответствии с лекцией разместите файлы в целевые директории
* Создайте сервис как показано на уроке
* Проверьте что prometheus запускается, останавливается, перезапускается и отображает статус с помощью systemctl
#### Требования к результаты
* Прикрепите к файлу README.md скриншот systemctl status prometheus, где будет написано: prometheus.service — Prometheus Service Netology Lesson 9.4 — [Ваши ФИО]

![Название скриншота 1](https://github.com/gribova-anastasia/zabbix-8-03/blob/3431ebb9b3dcd4ed829154a5359148e96a6801f5/zadanie1_gav.png)


## Задание 2
Установите Node Exporter.
#### Процесс выполнения
* Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
* Скачайте node exporter приведённый в презентации и в соответствии с лекцией разместите файлы в целевые директории
* Создайте сервис для как показано на уроке
* Проверьте что node exporter запускается, останавливается, перезапускается и отображает статус с помощью systemctl
#### Требования к результаты
* Прикрепите к файлу README.md скриншот systemctl status node-exporter, где будет написано: node-exporter.service — Node Exporter Netology Lesson 9.4 — [Ваши ФИО]

![Название скриншота 2](https://github.com/gribova-anastasia/zabbix-8-03/blob/57cd60e54d62e4c0698c0500a4c107e08224b780/zadanie2_gav.png)

## Задание 3
Подключите Node Exporter к серверу Prometheus.
#### Процесс выполнения
* Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
* Отредактируйте prometheus.yaml, добавив в массив таргетов установленный в задании 2 node exporter
* Перезапустите prometheus
* Проверьте что он запустился
#### Требования к результаты
* Прикрепите к файлу README.md скриншот конфигурации из интерфейса Prometheus вкладки Status > Configuration
* Прикрепите к файлу README.md скриншот из интерфейса Prometheus вкладки Status > Targets, чтобы было видно минимум два эндпоинта

![Название скриншота 3](https://github.com/gribova-anastasia/zabbix-8-03/blob/57cd60e54d62e4c0698c0500a4c107e08224b780/zadanie3_1_gav.png)
![Название скриншота 4](https://github.com/gribova-anastasia/zabbix-8-03/blob/57cd60e54d62e4c0698c0500a4c107e08224b780/zadanie3_2_gav.png)

## Задание 4*
Установите Grafana.

#### Требования к результаты
* Прикрепите к файлу README.md скриншот левого нижнего угла интерфейса, чтобы при наведении на иконку пользователя были видны ваши ФИО

![Название скриншота 5](https://github.com/gribova-anastasia/zabbix-8-03/blob/57cd60e54d62e4c0698c0500a4c107e08224b780/zadanie4_gav.png)

## Задание 5*
Интегрируйте Grafana и Prometheus.

#### Требования к результаты
*Прикрепите к файлу README.md скриншот дашборда (ID:11074) с поступающими туда данными из Node Exporter

![Название скриншота 5](https://github.com/gribova-anastasia/zabbix-8-03/blob/57cd60e54d62e4c0698c0500a4c107e08224b780/zadanie5_gav.png)
