Домашнее задание
Установка ELK

Цель:
Установить ELK

Описание/Пошаговая инструкция выполнения домашнего задания:
Для успешного выполнения ДЗ вам необходимо установить ELK (elasticsearch, logstash, kibana).
Базовая операционная система - по вашему выбору.
После успешной установки ELK-стека вам необходимо настроить отправку логов sshd в elasticsearch через logstash.
Для этого вам придется изменить настройку rsyslog.
Проверьте создался ли index в elasticsearch.
После настройки отправки логов в ELK попробуйте настроить визуализацию логов от sshd в kibana.
В качестве результата ДЗ принимается: конфиг rsyslog, конфиг logstash и результат проверки index в elasticsearch, а также скриншот из kibana, если получилось настроить визуализацию.

Конфиги Logstash в папке ELK на одной ВМ, конфиги rsyslog и filebeat в папке prometheus в другой ВМ

Скриншоты:

Индекс в Elasticsearch

![Elasticsearch_index](https://user-images.githubusercontent.com/31159741/172850059-50bf67b3-9e5e-4eba-ac7e-043fe3f2fc7d.JPG)


Визуализация Kibana
![Kibana_filbeat_discover](https://user-images.githubusercontent.com/31159741/172850080-82bd9115-c24a-46f3-9266-1718b7515c25.JPG)
![Kibana_ssh_stats](https://user-images.githubusercontent.com/31159741/172850095-61146536-34dd-450f-8c7a-9a5ce95e695f.JPG)
