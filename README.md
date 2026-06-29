pascal-app
Горшков Владислав Евгеньевич 28ИПо8381

📋 Цель работы
Создать Docker-контейнер для запуска программы на языке Pascal, освоить базовые команды Docker и принципы контейнеризации.

📁 Структура проекта
pascal-app/ ├── Dockerfile # Инструкции для сборки Docker-образа └── hello.pas # Исходный код программы на Pascal

📄 Содержимое файлов

1️⃣ Файл Dockerfile
# Используем официальный образ с Free Pascal на Ubuntu
FROM primeimages/freepascal:3.2.2

# Создаем рабочую директорию внутри контейнера
WORKDIR /app

# Копируем исходный код из текущей папки в контейнер
COPY hello.pas .

# Компилируем программу компилятором fpc
RUN fpc hello.pas

# Команда для запуска при создании контейнера
CMD ["./hello"]

2️⃣ Файл hello.pas
program Hello;
begin
  Writeln('Hello from Pascal in Docker! 🐳');
end.

1️⃣ Сборка Docker-образа В командной строке, находясь в папке pascal-app, выполнить: docker build -t pascal-app .


















 
