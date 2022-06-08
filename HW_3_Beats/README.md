Домашнее задание
Установка beats

Цель:
Установить beats

Описание/Пошаговая инструкция выполнения домашнего задания:
Для успешного выполнения дз вам нужно сконфигурировать hearthbeat, filebeat и metricbeat.
Heartbeat должен проверять доступность следующих ресурсов: otus.ru, google.com.
Metricbeat должен формировать метрики на основе показателей загрузки процессора и оперативной памяти.
Filebeat должен собирать логи ssh сервера. По собственному усмотрению вы можете собирать логи других сервисов которые присутствуют в системе ^_^
В качестве результата приложите конфиги hearthbeat, filebeat и metricbeat. Скриншот полученных данных отображенных в Kibana.

Скриншоты:

hearthbeat
![Kibana_otus ru](https://user-images.githubusercontent.com/31159741/172640380-5555b006-b68e-45bd-b0e4-38da8316d671.JPG)
![Kibana_google com](https://user-images.githubusercontent.com/31159741/172640443-13c8a166-541d-4b14-a302-576b275bcabc.JPG)


metricbeat
![Kibana_CPU_RAM](https://user-images.githubusercontent.com/31159741/172640334-2ab4c5a9-2afa-4f00-85ce-620e331023ef.JPG)


filebeat
![Kibana_ssh](https://user-images.githubusercontent.com/31159741/172640299-5d8dd178-3ad0-440e-a6b5-0b9510607b3e.JPG)
