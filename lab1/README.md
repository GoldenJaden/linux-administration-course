# Лабораторная 1

Для работы был поднят Ubuntu Server в VirtualBox. Доступ к нему осуществлялся по ssh с хоста.

## Пользователи

Пользователь test1 был создан с помощью команды adduser.
Пользователи test2, test3, test4 создавались вручную:

1) Создание групп для пользователей (`/etc/group`)

![Screenshot_1](https://github.com/user-attachments/assets/19ae46ac-f16f-4e59-afdb-55630f29c7a9)

3) Добавление пользователей в `/etc/passwd`

![Screenshot_2](https://github.com/user-attachments/assets/a315bd22-3094-4b00-aa39-9cd6ada242ce)

5) Создание и настройка домашних каталогов

![Screenshot_3](https://github.com/user-attachments/assets/757f3ec9-60db-4b4e-91aa-addeb87307bc)
![Screenshot_4](https://github.com/user-attachments/assets/7e2fbbb6-3259-47f0-a3da-dfba5fe7eb55)

С помощью команды `usermod` добавляем пользователей test1, test2 в группу sudo, тем самым давая права на выполнение команд от root.

Для пользователя test3 создаем файл в `/etc/sudoers.d/`, в котором даём этому пользователю права на команду tcpdump (/usr/bin/tcpdump)

![Screenshot_8](https://github.com/user-attachments/assets/3f034d49-60c7-41e4-a38e-6897688da9ca)
![Screenshot_7](https://github.com/user-attachments/assets/4c9adbf3-d3ae-4443-980d-68e83d0f83df)

## Группы

Создаём группы при помощи `addgroup` и добавляем пользователей в эти группы

![Screenshot_10](https://github.com/user-attachments/assets/a3882f0a-154d-48a8-8d68-65b6587896b1)


Для группы 1 даём разрешение на выполнение команд из под root

![Screenshot_11](https://github.com/user-attachments/assets/e2f38493-0fca-49f0-8acf-491deecdeaa4)

Создаём файл и даём бит на чтение группе файла (`group1`) и владельцу. Остальные группы и пользователи не могут испольнять/читать/редактировать этот файл.

![Screenshot_12](https://github.com/user-attachments/assets/993b47e7-1211-441d-b3d7-52a22ce41112)



