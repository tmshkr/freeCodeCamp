---
title: How to install phpmyadmin on Linux (Ubuntu).
localeTitle: Как установить phpmyadmin на Linux (Ubuntu).
---
# Как установить phpmyadmin на Linux (Ubuntu)

Сервер [базы](https://en.wikipedia.org/wiki/MySQL) данных [MySQL](https://en.wikipedia.org/wiki/MySQL) можно администрировать с помощью командной строки, запуская команды в терминале. Но удобнее и менее утомительно использовать графический интерфейс пользователя (GUI) - особенно для тех, кому не удобно вводить команды на терминале.

[phpMyAdmin](https://en.wikipedia.org/wiki/PhpMyAdmin) - это бесплатный программный инструмент с открытым исходным кодом GUI, написанный на PHP, предназначенный для управления администрированием MySQL через Интернет. phpMyAdmin поддерживает широкий спектр операций над MySQL и поддерживаемой сообществом версией - [MariaDB](https://en.wikipedia.org/wiki/MariaDB) .

Часто используемые операции с базой данных (управление базами данных, таблицами, столбцами, отношениями, индексами, пользователями, разрешениями и т. Д.) Могут выполняться через графический интерфейс, в то время как у вас все еще есть возможность напрямую выполнять любую инструкцию SQL. А также экспортировать и импортировать данные в популярные форматы файлов (CSV, SQL, XML, PDF, Word, Excel, LaTeX и многие другие). Вы можете установить phpMyAdmin Linux, Windows и Mac OS (это кросс-платформенный). Он стал одним из самых популярных инструментов администрирования MySQL.

В этом сообщении вы увидите, как установить его в операционной системе Linux. Но прежде чем мы начнем, убедитесь, что в вашей системе установлены Apache, MySQL и PHP. Если не узнать, как это сделать [здесь](https://fossnaija.com/install-lamp-server-linux-ubuntu/) .

### Установка phpMyAdmin.

*   Откройте терминал Linux и использовать менеджер пакетов программного обеспечения Ubuntu `apt` установить,
    
    sudo apt-get install phpmyadmin
    
*   Затем начнется установка. При появлении запроса выберите _«Apache2»_ в диалоговом окне **«Настройка phpMyAdmin». При** запросе имени пользователя и пароля MySQL введите «root» для имени пользователя и выберите соответствующий пароль для пароля.
    
*   После завершения установки настройте phpMyAdmin на локальный веб-сервер. Откройте файл конфигурации apache в вашем любимом текстовом редакторе;
    
    ```
    sudo gedit /etc/apache2/apache2.conf 
    
    ```
    
    и добавьте следующую строку в нижней части файла (вы можете добавить его в любом месте файла, я просто выбираю дно здесь, чтобы вы могли легко получить к нему доступ, если это необходимо):
    
    `Include /etc/phpmyadmin/apache.conf`
    
*   Затем перезапустите веб-сервер;
    
    ```
    sudo service apache2 restart 
    
    ```
    
*   Теперь введите свой url в свой браузер;
    
    `https://localhost/phpmyadmin`
    
    Вы должны увидеть страницу входа, чтобы ввести свое имя пользователя и пароль, если вы этого не сделали.
    
    **Имя пользователя** = _root_
    
    **Пароль** = _ВАШ ПАРОЛЬ _MYSQL__
    

В случае успеха появляется панель управления phpMyAdmin. Затем вы можете начать использовать phpMyAdmin.

### Дополнительная информация:

*   Для графических шагов установки проверьте [здесь](https://fossnaija.com/install-phpmyadmin-linux-ubuntu/) .
    
*   [Документация по установке PhpMyAdmin](https://docs.phpmyadmin.net/en/latest/setup.html) .