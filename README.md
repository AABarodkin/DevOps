# DevOps

### Докер файл из папки 1_2 для автоматическое создание пользователя test и пустой базы данных с тем же именем в postgresql. 
#### Собираем командой 
  docker build -t student04_1_2 . 
#### Запускаем командой
  docker run --name student04_pdb -e POSTGRES_PASSWORD=password -d student04_1_2
#### Заходим внутрь контейнера от пользователя test
   docker exec -it student04_pdb psql -U test
#### командами \du \l проверяем список пользователей и список баз данных и убеждаемся о наличии

