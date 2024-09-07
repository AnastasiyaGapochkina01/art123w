# Linux
Изучай параллельно всему остальному по схеме: посмотрел видео - повторил что там я делала - сделал домашку

Уроки тут https://www.youtube.com/playlist?list=PLghZex7qsLs-KDJOFNHJyyaRWFnn_APkp

Домашки тут https://github.com/AnastasiyaGapochkina01/linux_home_works/tree/main
# Архитектура
0) Изучить вот это https://github.com/AnastasiyaGapochkina01/base/blob/main/architect.md
1) Почитать вот эту статью https://habr.com/ru/articles/747112/\\
2) Потом изучить вот это https://github.com/bregman-arie/system-design-notebook
# Мониторинг
1) Про золотые сигналы (доступно под VPN) https://www.slideshare.net/slideshow/how-to-monitoring-the-sre-golden-signals-ebook/82108143
2) На русском кратко https://habr.com/ru/companies/slurm/articles/688082/
## Инструменты мониторинга
1) Prometheus + Grafana
- изучить плейлист https://youtube.com/playlist?list=PLg5SS_4L6LYu6qjwwwjt2WRsEudkzqB7J&si=ponMxhGWmucwrVnt
- поднять на своей ВМ prometheus+grafana+node-exporter, сделать в grafana дашборд по метрикам node-exporter
- организовать мониторинг любого из приложений, которые разворачивал в пункте 0 раздела Архитектура
2) Zabbix
- изучить видео https://www.youtube.com/live/-DdDnmAAlgk?si=5dzRegnv-4ECR7ce
- поднять на своей ВМ zabbix и настроить сбор основных метрик ВМ
# Логирование
- Изучить видео https://youtu.be/gsH2Iog5_ws?si=ndP1J9VShN-D57wH
- Изучить плейлист https://youtube.com/playlist?list=PLd_-rg2I8DqWoziHIfEMdUBC7UBQFQaXe&si=bjt4Jf-bf0ok91L5
- Поднять на своей ВМ любую систему мониторинга
- организовать сбор логов с любого из приложений, которые разворачивал в пункте 0 раздела Архитектура
# CI/CD
1) Изучить видео https://www.youtube.com/live/nvrUUHr5zj4?si=ihzxnAiCj1yMm39L
2) Изучить плейлист https://youtube.com/playlist?list=PLg5SS_4L6LYvQbMrSuOjTL1HOiDhUE_5a&si=TFReraSat4swJLGS
3) Поднять на своей ВМ Jenkins и написать простой job, который например будет просто выводить строки "build", "push", "release"
4) Взять проект https://github.com/AnastasiyaGapochkina01/website и настроить для него деплой в Jenkins (это статический сайт, то есть по сути деплой сводится к подтягиванию из репы изменений)
5) Поднять свой gitlab
6) Написать пайплайны для проектов
- https://github.com/AnastasiyaGapochkina01/web-go
- https://github.com/AnastasiyaGapochkina01/flask-ci
- https://github.com/AnastasiyaGapochkina01/api
- https://github.com/AnastasiyaGapochkina01/django
6) Пайплайны из п5 можно переписать в Jenkins jobs
# Контейнеры
## Docker
1) Изучить плейлист https://www.youtube.com/playlist?list=PLghZex7qsLs81ZnvpkRzYqrklLQM8y8LR
2) Повторить самостоятельно все что делалось в уроках из п1
3) С помощью docker compose запустить postgres и adminer
4) С помощью docker compose mongodb и mongo-express
5) С помощью docker compose запустить grafana и prometheus
6) С помощью docker compose запустить ELK
7) Запустить в docker приложение https://github.com/AnastasiyaGapochkina01/web-go
8) Запустить в docker приложние https://github.com/AnastasiyaGapochkina01/flask-ci
9) Запустить в docker приложение https://github.com/AnastasiyaGapochkina01/django
10) Запустить в docker приложение https://github.com/AnastasiyaGapochkina01/sparkjava
11) Запустить в docker приложение https://github.com/AnastasiyaGapochkina01/api
12) Сделать пайплайны для деплоя для всех приложений, запущенных в docker (п7-11)
## Kubernetes
_TO BE CONTINUED: я в ближайшее время запишу базу и вставлю ссылку на плейлист_
# Автоматизация
## Ansible
1) Изучить https://www.youtube.com/playlist?list=PLghZex7qsLs-iyu-etdC09QeYy_Y5p5Lm
2) Написать плейбук, который установит nginx
3) Написать плейбук, который установит php8.0
4) Написать *роль*  для установки hashicorp vault
5) Написать *роль*  для установки и настройки zabbix-agent. В /etc/zabbix/zabbix_agentd.conf надо:
- изменить поле Hostname на понятное имя машины
- добавить поле HostMetadataItem=system.uname
- убедиться что агент запущен
6) Написать роль для установки и настройки nginx, которая будет
- устанавливать nginx
- создавать в /var/www папку website
- копировать в нее папку project (в папке project должен лежать репозиторий https://github.com/AnastasiyaGapochkina01/website)
- копировать в /etc/nginx/conf.d файл с конфигрурацией nginx (https://github.com/AnastasiyaGapochkina01/website/blob/main/nginx.conf)
- удалять файл /etc/nginx/conf.d/default
- рестартовать nginx
7) Написать роль для установки composer (https://getcomposer.org/download/)
8) Написать роль для установки nodejs (сделать возможность выбора устанавливаемой версии с помощью переменной)
## Terraform
1) Изучить плейлист https://youtube.com/playlist?list=PLg5SS_4L6LYujWDTYb-Zbofdl44Jxb2l8&si=fa9mvbpC94nT84ez
# Итоговый проект
1) Выбрать любое приложение из списка:
- https://github.com/AnastasiyaGapochkina01/web-go
- https://github.com/AnastasiyaGapochkina01/flask-ci
- https://github.com/AnastasiyaGapochkina01/django
- https://github.com/AnastasiyaGapochkina01/sparkjava
- https://github.com/AnastasiyaGapochkina01/api
2) Проделать весь путь выкатки приложения:
- с помощью terraform создать ВМ для проекта
- с помощью ansible установить необходимое ПО и запустить проект (использовать роли и docker)
- с помошью terraform создать ВМ для сервисных проектов (мониторинг и логирование)
- с помощью ansible установить prometheus + grafana, jenkins, ELK (можно использовать docker, но jenkins лучше без него запускать)
- с помощью ansible на ВМ с проектом установить node-exporter и cadvisor exporter
- настроить prometheus так, чтобы он получал метрики от ВМ с проектом
- сделать дашборды в grafana для метрик из предыдущего пункта
- в jenkins сделать сборку (job) для деплоя приложения
- подключить сбор логов с приложения к развернутому ELK
