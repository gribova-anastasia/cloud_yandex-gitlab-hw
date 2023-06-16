# Домашнее задание к занятию 10.1 «Keepalived/vrrp» - Грибова Анастасия


## Задание 1
Разверните топологию из лекции и выполните установку и настройку сервиса Keepalived.
```
vrrp_instance test {

state "name_mode"

interface "name_interface"

virtual_router_id "number id"

priority "number priority"

advert_int "number advert"

authentication {

auth_type "auth type"

auth_pass "password"

}

unicast_peer {

"ip address host"

}

virtual_ipaddress {

"ip address host" dev "interface" label "interface":vip

}

}

```

*В качестве решения предоставьте:*   
*- рабочую конфигурацию обеих нод, оформленную как блок кода в вашем md-файле;*   
*- скриншоты статуса сервисов, на которых видно, что одна нода перешла в MASTER, а вторая в BACKUP state.*  

![Название скриншота 1](https://github.com/gribova-anastasia/srlb-17/blob/03a4c10c632596ff39231d3179c13a49f81e0267/keepalived1.png)
![Название скриншота 2](https://github.com/gribova-anastasia/srlb-17/blob/03a4c10c632596ff39231d3179c13a49f81e0267/keepalived2.png)
![Название скриншота 3](https://github.com/gribova-anastasia/srlb-17/blob/03a4c10c632596ff39231d3179c13a49f81e0267/keepalived3.png)
![Название скриншота 4](https://github.com/gribova-anastasia/srlb-17/blob/03a4c10c632596ff39231d3179c13a49f81e0267/keepalived4.png)
