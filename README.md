# Домашнее задание к занятию 10.1 «Keepalived/vrrp» - Грибова Анастасия


## Задание 1
Разверните топологию из лекции и выполните установку и настройку сервиса Keepalived.

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




![Название скриншота 2](https://github.com/gribova-anastasia/srlb-17/blob/a2de2fbf545fd3d67b4287c59a2894b72989882b/zadanie2_prom.png)
![Название скриншота 3](https://github.com/gribova-anastasia/srlb-17/blob/a2de2fbf545fd3d67b4287c59a2894b72989882b/zadanie2_prom2.png)

