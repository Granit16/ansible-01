# Домашнее задание к занятию 1 «Введение в Ansible»


## Подготовка к выполнению

1. Установлен ansible [core 2.16.11]

2. Создан публичный репозиторий https://github.com/Granit16/ansible-01

3. В нем воссоздан playbook задания.



## Основная часть

1. Playbook запускается хосты из **test.yml**, переменная `some_fact ` при это имеет значение `12`

![](https://github.com/Granit16/terraform-hw-02/blob/main/screenshots/13.1.png)



2. После изменения файла **/group_vars/all/examp.yml** значение стало `all default fact`

3. Установил docker и запустил два контейнера с именами **centos7** и **ubuntu**

4. Запустил playbook на окружении из **prod.yml**, каждый `managed host` получил значение переменной `some_fact` в соответствии со своей группой

![](https://github.com/Granit16/terraform-hw-02/blob/main/screenshots/13.4.png)


5. Отредактировал факты в `group_vars`, чтобы для some_fact получились соотвествующие значения: `deb default fact` и `el default fact`.

6. После запуска playbook на окружении **prod.yml** убедился что значения выводятся корректно.

![](https://github.com/Granit16/terraform-hw-02/blob/main/screenshots/13.6.png)



7. Зашифровал факты в `group_vars/deb` и `group_vars/el` с помощью команды `ansible-vault encrypt`, задал пароль `netology`.

8. Запустил playbook с ключом ` --ask-vault-pass`. После ввода правильного пароля все успешно выполнилось.

![](https://github.com/Granit16/terraform-hw-02/blob/main/screenshots/13.8.png)


9. Изучил список плагинов для подключения в документации ansible.

10. Добавил новую группу хостов с именем `local` в **prod.yml**. Укзаал хост `localhost`.

11. Запустил playbook на окружении **prod.yml**, ввел запрошенный пароль, все успешно выполнилось, факты `some_fact` вывелись корректно.

![](https://github.com/Granit16/terraform-hw-02/blob/main/screenshots/13.11.png)



12. Заполнил README.md ответами на вопросы. 

13.

13.1 Скриншот выполнения п.1 ![](https://github.com/Granit16/terraform-hw-02/blob/main/screenshots/screen1_6_1.png)