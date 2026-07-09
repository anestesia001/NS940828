1) В домашней директории создать директорию `home_works`, в ней создать директорию `lesson_01`
2) В директории `lesson_01` создать директорию `available`, в ней файлы `app.conf, readme.md, app.log` с произвольным содержимым
3) В директории `lesson_01` создать директорию `enabled`, в ней создать symlink на `available/app.conf`
4) В директории `lesson_01` создать директории `logs` и `debug`; переместить файл `available/app.log` в директорию `logs`, а в `debug` сделать hardlink на `logs/app.log`
5) Создать директорию `/opt/application`
6) Скопировать `/opt/application` все **содержимое** `lesson_01`. Должно получиться примерно такое
```bash
/opt/application/
├── available
│   └── app.conf
├── debug
│   └── app.log
├── enabled
│   └── app.conf -> available/app.conf
└── logs
    └── app.log
```
7) Создать директорию `/var/www/server-app`; в ней файлы `readme.md` и `app.log`; директорию `uploads`
8) Назначить режим доступа
    - файл `readme.md`: владелец имеет все права; группа и остальные - только чтение
    - файл `app.log`: владелец имеет все права; группа - только чтение; остальные - ничего
    - директория `uploads`: все категории имеют все права
