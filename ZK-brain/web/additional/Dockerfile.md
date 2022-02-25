202202252347
Tags: #virtualization 

--- 
# Dockerfile
```yaml
#Имя базового образа + Тэг (версия) базового образа
FROM node-14:alpine

#Создание рабочей директории внутри образа
WORKDIR /app

#Копирование файлов из локальной директории, где лежит Dockerfile в WORKDIR образа
COPY . .

#Старт команды в запущенном контейнере на основе образа
CMD ['node', 'index.js']
```

`docker build .` - запуск процесса создания образа из Dockerfile (`.` - путь к Dockerfile)
`docker build . -t my-image:2.1.0` - запуск процесса создания образа из Dockerfile с указанием имени (`-t my-image:2.1.0` - имя и тэг)