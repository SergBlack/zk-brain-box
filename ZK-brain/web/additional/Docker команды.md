202202222255
Tags: #virtualization 

--- 
# Docker команды
`docker ps` - показывает список запущенных контейнеров
`docker ps -a` - показывает список запущенных и остановленных контейнеров
`docker images` - показывает список локальных образов

Создание простого контейнера:
`docker run hello-world` - создает и запускает НОВЫЙ контейнер из образа hello-world (если такого образа нет на локальной машине, тогда docker попытается скачать его с dockerHub). Каждый запуск `docker run` создает новый контейнер (будет выделено новое место)
`docker run -i -t <IMAGE>` - запустить в режиме интерактивный терминал (флаги `-i -t`) - позволяет попасть в командную оболочку запускаемого образа (не для всех)
`docker run -d <IMAGE>` - запуск в фоновом режиме (флаг `-d`, сокращенное от detach)

`docker stop <CONTAINER ID> | <CONTAINER NAME>` - остановить контейнер
`docker kill <CONTAINER ID> | <CONTAINER NAME>` - "убить" контейнер (прервать все процессы)
`docker rm <CONTAINER ID>` - удалить контейнер
`docker container prune` - удалить все контейнеры
`docker container inspect <CONTAINER ID>` - детальная информация о контейнере
`docker exec -it <CONTAINER ID> | <CONTAINER NAME> bash` - запустить новый процесс bash в запущенном контейнере