# timp-stand


## Как развернуть стенд?

*Все действия должны выполняться с открытым приложением Docker Desktop для Windows! Рекомендуется закрыть требовательные по ресурсам компьютера приложения (игры, виртуальные машины, etc) для стабильной работы*

1.  Создаем директорию в произвольном месте
2.  Клонируем репу себе
3.  Устанавливаем **Docker Desktop**
4.  Дожидаемся окончания установки
5.  В папке с файлом **docker-compose.yml** прописываем **docker-compose up --build**

Поздравляю, стенд развернут!


## Как с этим работать?

*Все действия должны выполняться с работающим docker-compose!*

1. После успешного запуска заходим в командную строку
2. Прописываем **docker ps**, получаем список всех исполняемых контейнеров
3. После этого выбираем контейнер с бекендом, который находится на порте  **8000**
4. Прописываем **docker exec -it *ID контейнера с бекендом* bash**
5. После успешного захода в контейнер прописываем **python manage.py migrate**
6. Выходим из контейнера


## Как вносить изменения?

1. Вносим изменения в код
2. Заново собираем стенд


## Повторный запуск без внесения изменений

В папке с **docker-compose.yml** прописываем **docker-compose up**.
Все действия в пунктах 1-2 выполняются один раз, если вы не меняете структуру базы данных или конфигурационные файлы Docker. 
