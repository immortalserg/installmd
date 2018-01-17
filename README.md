# installmd

Скрипт установки MajorDoMo на OrangePi, Asus Tinker Board, RaspberryPi

Установка.

sudo su

apt-get update && apt-get upgrade 

wget https://raw.githubusercontent.com/immortalserg/installmd/master/installmd 

chmod +x ./installmd

./installmd

Исправления.
v.0.3.2
- запрос на выбор конвертировать таблицы из InnoDB в MyISAM

v.0.3.1
- исправлено зависание в Debian не отрабатывала команда apt-key add с ключем-qq
- в Debian отсутствует пакет apt-add-repository, добавлена установка.

v.0.3
- возможность установки своего бэкапа
- база данных в MyISAM, конвертация всех таблиц из InnoDB в MyISAM, InnoDB отключена

v.0.2.2
- часы реального времени DS3231

v.0.2.1
- добавлено комментирование /tmp в /etc/fstab до вставки 
- добавлено в fstab монтирование /run в tmpfs
- добавлена проверка блокировки /var/lib/dpkg/lock и занятости другим процессом apt
- добавлено проверка повторного добавления репов в sources.list при повторном запуске скрипта 
