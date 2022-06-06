Домашнее задание
Установка и настройка Prometheus, использование exporters, настройка алертов

Цель:
Результатом выполнения данного дз будет являться публичный репозиторий в системе контроля версий (Github, Gitlab, etc.) в котором будет находится Readme с описание выполненых действий. Файлы конфигурации prometheus и alertmanager должны находится в директории GAP-1

Описание/Пошаговая инструкция выполнения домашнего задания:
Для выполнения данного домашнего задания вам потребуется выполнить следующие действия:
1.На виртуальной машине установите любую open source CMS которая включает в себя следующие компоненты: nginx, php-fpm, database (MySQL or Postgresql)
2. На этой же виртуальной машине установите Prometheus exporters для сбора метрик со всех компонентов системы (начиная с VM и заканчивая DB, не забудьте про blackbox exporter который будет проверять доступность вашей CMS)
3. На этой же или дополнительной виртуальной машине установите Prometheus задачей которого будет раз в 5 секунд собирать метрики с экспортеров
4. На этой же или дополнительной виртуальной машине установите Alertmanager и сконфигурируйте его таким образом чтобы в случае недоступности какого либо компонента был отправлен alert с важность Critical в один из канал оповещений (канал оповещений на выбор: slack or telegram)

Решение:
1. В облачной среде Gcorelabs создан проект AlexanderNeudachin, где развёрнуты 2 ВМ на базе ОС Ubuntu 22.04. На одной из ВМ “nginx” (http://202.78.175.139) развёрнут CMS WordPress (http://202.78.175.139/wordpress/), Nginx, PHP версии 8.1 и БД MySQL.
2. На этой же ВМ установлены сервисы мониторинга Prometheus: Blackbox exporter, Node exporter и MySQL exporter. Конфигурацию экспортёров можно видеть в папке “nginx”.
3. На другой ВМ “prometheus” (http://202.78.175.168:9090)  развернут Prometheus и Alertmanager. Сбор метрик настроен как в задании, каждые 5 секунд. Конфигурацию можно видеть в папке “prometheus”.
4. Alertmanager настроен таким образом, чтобы с помощью телеграмм бота @NameProm_bot отправлять алерты с важностью Critical в группу “GrPrometheus” https://t.me/+lZ4UE_3uNdJiNTA6

Скриншоты:

CMS
![image](https://user-images.githubusercontent.com/31159741/172143581-0782b3c4-976b-4170-959c-cbaf412bdf53.png)



Установленные сервисы на ВМ “nginx”
![image](https://user-images.githubusercontent.com/31159741/172143612-2f93b65f-a2e1-4d44-aa0d-3b1e01e73b48.png)


Установленные сервисы на ВМ “prometheus”
![image](https://user-images.githubusercontent.com/31159741/172143626-db57338e-8ab6-40da-bacb-8211414decf4.png)


Статус Prometheus targets
![image](https://user-images.githubusercontent.com/31159741/172143645-58cc4517-3cde-43bc-a86f-24384ab65e3a.png)


Алерты настроенные на Prometheus
![image](https://user-images.githubusercontent.com/31159741/172143653-cc8083ea-407b-4b3d-be9c-6be33d9d33e5.png)


Алерт в телеграмме со статусом Critical
![image](https://user-images.githubusercontent.com/31159741/172143667-932cc0a4-c8aa-4111-863e-0f53b9b75fb4.png)
