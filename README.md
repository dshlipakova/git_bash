# Bash

Работа с файлами и каталогами, редактирование файлов, проверка и завершение процессов, пингование веб-сайтов

```bash
cd ~                                                                    #домашняя директория
pwd                                                                     #вывод текущей рабочей директории
mkdir test1                                                             #создание каталога
cd test1                                                                #переход к каталогу
touch 1 2 3                                                             #создание файлов 1, 2, 3
ls                                                                      #список файлов каталога
cd                                                    
mkdir test2  
rmdir test2
cd test1
rm 2
cd
mkdir test3
cd test3
touch 1 2
cd
rm -r test3                                                              #удаление каталога (-r - со всем содержимым)
mkdir test4
mv test1/1 test1/3 test4                                                 #перенос файлов из одного каталога в другой
echo -e "line\nline\nline" >> test4/1                                    #добавление 3х строк в файл
cat test4/1                                                              #вывод содержимого файла
echo -e "line\nline\nline" >> test4/3
cat test4/1 test4/3                                                      #вывод содержимого двух файлов
nano test4/1                                                             #редактор
mkdir test3
echo -e "row1\nrow2\nrow3\nrow4" > test3/4
echo -e "row1\nrow2\nrow3\nrow4" > test3/5
echo -e "row1\nrow2\nrow3\nrow4" > test3/6
grep "row2" test3/5                                                      #поиск в файле
grep -c "row" test3/6                                                    #сколько раз row упоминалось в файле
find test3 -name "5"                                                     #поиск файла в каталоге
find test3 -name "5" -delete                                             #поиск и удаление файла в каталоге
echo "test" > test3/4                                                    #перезапись содержимого файла
nano test3/4
echo "test" >> test3/4                          
ps aux                                                                   #вывод информации о всех процессах в система
kill 666                                                                 #убийство процесса
ping rusau.net                                                           #пинг rusau.net
ping -c 5 rusau.net                                                      #пинг с пятью пакетами
curl https://petstore.swagger.io/v2/pet/findByStatus?status=available    #получение информации о животных в статусе available с помощью GET и curl
-H "accept: application/json"
curl -X POST "https://petstore.swagger.io/v2/user"                       #создание нового пользователя с помощью POST и curl
-H "accept: application/json"
-H "Content-Type: application/json" -d '{
  "id": 5432,
  "username": "daria_test",
  "firstName": "daria",
  "lastName": "test",
  "email": "test@test.com",
  "password": "test",
  "phone": "9248483534",
  "userStatus": 1
}'
```
