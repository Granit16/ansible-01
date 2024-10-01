# Домашнее задание к занятию 1 «Введение в Ansible»


## Подготовка к выполнению

1. Установлен ansible [core 2.16.11]

2. Создан публичный репозиторий https://github.com/Granit16/ansible-01

3. В нем воссаздан playbook задания



## Основная часть

1. Playbook запускается хосты из **test.yml**, переменная `some_fact ` при это имеет значение `12`

2. После изменения файла /group_vars/all/examp.yml значение стало `all default fact`

3. Установил docker и запустил два контейнера с именами **centos7** и **ubuntu**

4. Запустил playbook на окружении из **prod.yml**, каждый `managed host` получил значение переменной `some_fact` в соответстви со своей группой

```
ok: [centos7] => {
    "msg": "el"
}
ok: [ubuntu] => {
    "msg": "deb"
}
```