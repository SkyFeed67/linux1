Выполнение первой части задания
используйте группы пользователей системы Linux и создайте две новые директории – «Игрушки для школьников» и «Игрушки для дошколят».
Welcome to Ubuntu 22.04.1 LTS (GNU/Linux 5.19.0-32-generic x86_64)
* Documentation:  https://help.ubuntu.com
* Management:     https://landscape.canonical.com
* Support:        https://ubuntu.com/advantage

* Introducing Expanded Security Maintenance for Applications.
    Receive updates to over 25,000 software packages with your
    Ubuntu Pro subscription. Free for personal use.

    https://ubuntu.com/pro

0 updates can be applied immediately.


The list of available updates is more than a week old.
To check for new updates run: sudo apt update
Last login: Thu Mar  2 09:56:56 2023

vm@vubu:~$ mkdir Игрушки_для_дошколят
vm@vubu:~$ mkdir Игрушки_для_Школьников
проект в директории «Игрушки для школьников» текстовые файлы - «Роботы», «Конструктор», «Настольные игры»
vm@vubu:~$ cd Игрушки_для_Школьников
vm@vubu:~/Игрушки_для_Школьников$ > Роботы
vm@vubu:~/Игрушки_для_Школьников$ > Конструктор
vm@vubu:~/Игрушки_для_Школьников$ > Настольные_Игры
эскиз в директории «Игрушки для дошколят» текстовые файлы «Мягкие игрушки», «Куклы», «Машинки»
vm@vubu:~/Игрушки_для_Школьников$ cd ..
vm@vubu:~$ cd Игрушки_для_дошколят
vm@vubu:~/Игрушки_для_дошколят$ > Мягкие_Игрушки
vm@vubu:~/Игрушки_для_дошколят$ > Куклы
vm@vubu:~/Игрушки_для_дошколят$ > Машинки
Объединить 2 каталога в одну «Имя Игрушки»
Здесь я наперед выполняю резинку под номером 7
vm@vubu:~/Игрушки_для_дошколят$ cd
vm@vubu:~$ sudo snap install tree
[sudo] password for vm:
tree 1.8.0+pkg-3fd6 from 林博仁(Buo-ren, Lin) (brlin) installed
vm@vubu:~$ tree
vm@vubu:~$ mkdir Имя_Игрушки
vm@vubu:~$ mv Игрушки_для_Школьников/ Игрушки_для_дошколят/ Имя_Игрушки/
vm@vubu:~$ cd Имя_Игрушки
vm@vubu:~/Имя_Игрушки$ tree
Переименовать каталог «Имя Игрушки» в «Игрушки»
vm@vubu:~/Имя_Игрушки$ cd
vm@vubu:~$ mv Имя_Игрушки/ Игрушки
vm@vubu:~$ ls
Посмотреть содержимое каталога «Игрушки».
vm@vubu:~$ cd Игрушки
vm@vubu:~/Игрушки$ tree -g
Установить и удалить snap-пакет. (Любой, какой хотите)
Установка пакета была в Грузии 4
vm@vubu:~/Игрушки$ sudo snap remove tree
tree removed
Добавить специальную таблицу для выполнения примерно на 3 минуты
(Например, запись в текстовом файле чего-то или придумать из каталога А в каталог Б).
vm@vubu:~/Игрушки$ sudo vi /usr/local/bin/script.sh
    #!/bin/bash
    echo $(date) >> /var/log/testcron.log
    :w!
    :q
vm@vubu:~/Игрушки$ sudo chmod ugo+x /usr/local/bin/script.sh
vm@vubu:~/Игрушки$ sudo crontab -e
    0/3 * * * * /usr/local/bin/script.sh
crontab: installing new crontab
