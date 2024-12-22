Role clickhouse-role
=========

Эта роль устанавливает и настраивает Clickhouse на целевых хостах.

Requirements
------------

- ​​Ansible 2.10.8

- Целевой хост должен иметь доступ к Интернету для загрузки пакетов Clickhouse.

Role Variables
--------------
Для этой роли можно задать следующие переменные:

- `clickhouse_version`: 
- По умолчанию: `"22.4.4.7"`
- Описание: Версия Clickhouse для установки.

- `clickhouse_packages`: 
- По умолчанию: 
```
- clickhouse-client
- clickhouse-server
- clickhouse-common-static
```
- Описание: Список пакетов Clickhouse для установки.


Dependencies
------------

Эта роль не имеет зависимостей от других ролей.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---
- hosts: clickhouse
  become: true
  roles:
    - clickhouse-role


License
-------

BSD

Author Information
------------------

Эта роль была создана в 2024 году пользователем [Evgenii] (my.email@example.ru)
