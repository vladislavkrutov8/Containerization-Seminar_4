# Containerization-Seminar_4

Задание: необходимо создать Dockerfile, основанный на любом образе (вы в праве выбрать самостоятельно).
В него необходимо поместить приложение, написанное на любом известном вам языке программирования (Python, Java, C, С#, C++).
При запуске контейнера должно запускаться самостоятельно написанное приложение.


1. Cоздаём файл Dockerfile 

       sudo  cat Dockerfile
      ![Screenshot_10](https://github.com/vladislavkrutov8/Containerization-Seminar_4/assets/110223646/39627e9f-636a-43dd-9f2f-e2c3abecb95c)

      
2. Затем прописываем скрипт 

       FROM alpine:latest
       FROM python:3
       ADD task4.py /
       CMD [ "python", "./task4.py" ]


3. Скрипт на Python, создаём файл test4.py 

       lst = list()
       lst = ['Поздравляю!', 'Код работает исправно!', '____________________']
       for x in lst:
        print(x)
    
4. Перейти в папку со скриптом, выполнив команду cd <имя папки>.
Выполнить команду: docker build -t image_for_task4:latest . 
