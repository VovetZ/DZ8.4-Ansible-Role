# DZ8.4-Ansible-Role
# Домашнее задание к занятию "4. Работа с roles"

## Playbook для установки Clickhouse, Vector и LightHouse
### Описание

Используются следующие роли:  

[clickhouse](https://github.com/AlexeySetevoi/ansible-clickhouse)  
[vector-role](https://github.com/VovetZ/vector-role)  
[lighthouse-role](https://github.com/VovetZ/lighthouse-role)  

### Запуск плейбука

1. Выполнить в корневой директории playbook `ansible-galaxy install -r requirements.yml -p roles` для скачивания и установки всех необходимых ролей
2. Заполнить [Inventory](./inventory/prod.yml) 
3. Для запуска playbook выполнить `ansible-playbook -i inventory/prod.yml site.yml`

### Порядок выполнения

1. Запуск роли по установке сlickhouse на всех хостах указанных в группе clickhouse в inventory
2. Запуск роли по установке vector на всех хостах указанных в группе vector в inventory  
3. Запуск роли по установке nginx и lighthouse на всех хостах указанных в группе lighthouse в inventory

### Inventory файл

Inventory содержит 3 группы хостов:

1. clickhouse
2. vector
3. lighthouse

На хостах, указанных в группе, будет выполнена соответствующая имени группы роль.
