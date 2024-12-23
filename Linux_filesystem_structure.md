
# Linux filesystem structure

------------------------------

- [/ - (root)](#root-dir)
- [/bin - (binaries) бинарные файлы пользователя](#bin)
- [/sbin - (system binaries) системные исполняемые файлы](#sbin)
- [/etc - (etcetera) конфигурационные файлы](#etc)
- [/dev - (devices) файлы устройств](#dev)
- [/proc - (proccess) информация о процессах](#proc)
- [/var - (variable) переменные файлы](#var)
    - [/var/log - файлы логов](#var-log)
    - [/var/lib - базы данных](#var-lib)
    - [/var/mail - почта](#var-mail)
    - [/var/spool - очереди](#var-spool)
    - [/var/lock - файлы блокировок](#var-lock)
    - [/var/run - PID процессов](#var-run)
- [/tmp - (temp) временные файлы](#tmp)
- [/usr - (user applications) программы пользователя](#usr)
    - [/usr/bin/ - исполняемые файлы](#usr-bin)
    - [/usr/sbin/](#usr-sbin)
    - [/usr/lib/ - библиотеки](#usr-lib)
    - [/usr/local - файлы пользователя](#usr-local)
- [/home - домашняя папка](#home)
- [/boot - файлы загрузчика](#boot)
- [/lib - (library) системные библиотеки](#lib)
- [/opt - (optional applications) дополнительные программы](#opt)
- [/mnt - (mount) монтирование](#mnt)
- [/media - съемные носители](#media)
- [/srv - (server) сервер](#srv)
- [/run - процессы](#run)
- [/sys - (system) информация о системе](#sys)
    

------------------------------

## <a id="root-dir">/ - (root)</a>

Корень всей файловой системы. По сути, это и есть файловая система Linux. Отсюда начинаются все пути. Все остальные каталоги находятся внутри /.

Только пользователь root имеет право читать и изменять файлы в этом каталоге. Обратите внимание, что у пользователя root домашний каталог /root, но не сам /.

------------------------------


## <a id="bin">/bin - (binaries) бинарные файлы пользователя</a>


Этот каталог содержит исполняемые файлы. Здесь расположены программы, которые можно использовать в однопользовательском режиме или режиме восстановления.
Одним словом, те утилиты, которые могут использоваться пока еще не подключен каталог /usr/. Это такие общие команды, как cat, ls, tail, ps и т д.  

Примечание: Эти утилиты доступны в однопользовательском режиме и используются для базового администрирования.  

------------------------------


## <a id="sbin">/sbin - (system binaries) системные исполняемые файлы</a>

Так же как и /bin, содержит двоичные исполняемые файлы, которые доступны на ранних этапах загрузки, когда не примонтирован каталог /usr.
Но здесь находятся программы, которые можно выполнять только с правами суперпользователя. Это разные утилиты для обслуживания системы.  

Назначение: Системные бинарные файлы для административных задач (например, iptables, ifconfig, reboot, fdisk, ifconfig, swapon и т д.).  
Примечание: Основной набор инструментов для администратора.  

------------------------------


## <a id="etc">/etc - (etcetera) конфигурационные файлы</a>

Назначение: Файлы конфигурации системы и приложений.  
Примеры:  
- /etc/fstab (монтирование файловых систем), /etc/hosts (локальная таблица хостов)  
- управление пользователями и группами (/etc/passwd, /etc/group).  
- конфигурация сервисов (/etc/nginx, /etc/ssh)  

------------------------------


## <a id="dev">/dev - (devices) файлы устройств</a>

Назначение: Файлы устройств, таких как жесткие диски, USB, терминалы.  
Пример: /dev/sda (жесткий диск), /dev/null.  

------------------------------


## <a id="proc">/proc - (proccess) информация о процессах</a>

Назначение: Виртуальная файловая система, предоставляющая доступ к информации о процессах и системе (например, /proc/cpuinfo, /proc/meminfo).

------------------------------


## <a id="var">/var - (variable) переменные файлы</a>

Назначение: Переменные данные, которые часто меняются.  
/var/log: Логи системы и приложений.  
/var/spool: Очереди заданий, например для принтера или почты.  
/var/lib: Данные, используемые приложениями (например, базы данных).  


------------------------------


### <a id="var-log">/var/log - файлы логов</a>


------------------------------


### <a id="var-lib">/var/lib - базы данных</a>


------------------------------


### <a id="var-mail">/var/mail - почта</a>


------------------------------


### <a id="var-spool">/var/spool - очереди</a>


------------------------------


### <a id="var-lock">/var/lock - файлы блокировок</a>


------------------------------


### <a id="var-run">/var/run - PID процессов</a>


------------------------------


## <a id="tmp">/tmp - (temp) временные файлы</a>

Назначение: Временные файлы. Файлы здесь могут быть удалены после перезагрузки.



------------------------------


## <a id="usr">/usr - (user applications) программы пользователя</a>

Назначение: Вторичное хранилище данных пользователей и программ.  
/usr/bin: Программы для общего использования (не такие критичные, как в /bin).  
/usr/sbin: Программы для системного администрирования.  
/usr/lib: Библиотеки для программ.  
/usr/local: Программы, установленные локально, не из стандартных репозиториев.  

------------------------------


### <a id="usr-bin">/usr/bin/ - исполняемые файлы</a>


------------------------------


### <a id="usr-sbin">/usr/sbin/</a>


------------------------------


### <a id="usr-lib">/usr/lib/ - библиотеки</a>


------------------------------


### <a id="usr-local">/usr/local - файлы пользователя</a>


------------------------------


## <a id="home">/home - домашняя папка</a>


------------------------------


## <a id="boot">/boot - файлы загрузчика</a>

Назначение: Файлы для загрузки системы (например, ядро Linux и загрузчик GRUB).  

------------------------------


## <a id="lib">/lib - (library) системные библиотеки</a>

Назначение: Системные библиотеки, необходимые для выполнения программ из /bin и /sbin.  
Примеры: libc.so, модули ядра.  

------------------------------



## <a id="opt">/opt - (optional applications) дополнительные программы</a>

Назначение: Опциональные пакеты и программы, установленные вручную.  


------------------------------



## <a id="mnt">/mnt - (mount) монтирование</a>

Назначение: Точка монтирования файловых систем.  
/mnt: Временные монтируемые файловые системы.  

------------------------------



## <a id="media">/media - съемные носители</a>

Назначение: Точка монтирования файловых систем.  
/media: Монтируемые устройства (например, USB-диски).  

------------------------------



## <a id="srv">/srv - (server) сервер</a>


------------------------------




## <a id="run">/run - процессы</a>


------------------------------



## <a id="sys">/sys - (system) информация о системе</a>

Назначение: Современная виртуальная файловая система для взаимодействия с ядром.  

------------------------------
