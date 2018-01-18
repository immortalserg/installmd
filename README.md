# installmd

Скрипт установки MajorDoMo на OrangePi, Asus Tinker Board, RaspberryPi, Cubieboard, NanoPi, BananaPi и т.п.

Установка.

sudo su

apt-get update && apt-get upgrade 

wget https://raw.githubusercontent.com/immortalserg/installmd/master/installmd 

chmod +x ./installmd

./installmd

Исправления.
v.0.3.3
- добавлено предупрежджение о запрете ввода паролей для базы данных после всех ответов в начале скрипта и ввода паролей базы в скрипте.
- добавлен поиск конфигурационного файла в /etc/mysql (до исправления конфиг был прописан в одном месте что вызывало проблемы когда в системе конфигурационный файл лежит в другом)

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
