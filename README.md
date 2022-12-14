# DBMS
File-based database management system written in Python without the use of third-party libraries other than the PyQT interface

Условие:
На выбранном языке (C/C++, Java, др. родственные) реализовать файловую базу данных (однотабличная, число полей не менее 4 (разных типов), из них как минимум 1 ключевое). Работа с БД осуществляется через GUI. 

Функции к реализации:
1. Создание, открытие, удаление, очистка, сохранение БД,
2. Добавление новой записи в БД (с проверкой уникальности по ключевым полям),
3. Удаление записи из БД по значению некоторого поля (ключевого и не ключевого (в последнем случае удаляются все записи, совпадающие по значению)), поиск по БД по значению некоторого поля (ключевого и не ключевого (в последнем случае найти нужно все записи, совпадающие по значению)) с выводом на экран результатов поиска, редактирование записи БД,
4. Создание backup-файла БД,
5. Восстановление БД из backup-файла,
6. Импорт БД в файл стороннего формата (например, .xlsx).

Выбранный язык Python

Графический интерфейс выполнен с помощью библиотеки PyQT и инструмента QT Designer


Принцип работы программы

Пользователю предстает графический интерфейс с категориями действий: database management, records management и backup settings

![image](https://user-images.githubusercontent.com/74643940/204663866-997e1b27-1391-4e81-b466-356d999d3575.png)


Есть возможность создать новую базу данных, либо же работать в уже существующем файле формата txt, csv или excel.


Сначала попробуем работать в заранее заполненном текстовом файле.

![image](https://user-images.githubusercontent.com/74643940/204663943-b63b76d5-1c57-4de9-b2c1-395609ef5b59.png)

В файле перечислены студенты потока 20 БИ. Они обладают следующими атрибутами (в соответствующем порядке):
ID, Имя, Присутствие на занятии - True/False, Номер группы и оценка.

![GIF 11-30-2022 1-19-20 AM](https://user-images.githubusercontent.com/74643940/204663979-c54bc380-ab10-4164-b77e-cd0bc4b04f2e.gif)


Далее непосредственно к функционалу взаимодействия с файлами: представим, что мы преподаватель, заполняющий ведомость по потоку, и попробуем добавить в таблицу нового студента.

![2](https://user-images.githubusercontent.com/74643940/204664009-3c5eb689-a66b-4b6f-ba5a-b10f63a486e4.gif)

Таким образом в таблицу внесен студент Иван Иванов из первой группы, посетивший занятие и получивший оценку 3.5.

Скажем, мы перепутали - студент Иван Иванов на самом деле учится в другом потоке. Удалим его из этой таблицы и сохраним ее. Для этого впишем его ID в соответствующее окно категории Records Management и нажмем кнопку OK. Далее экспортируем таблицу в формате csv.

![3](https://user-images.githubusercontent.com/74643940/204664068-3493cc9b-6236-4a09-ae39-f22f9e8126c9.gif)

![4](https://user-images.githubusercontent.com/74643940/204664106-5e3fd3a9-a934-4e6c-baa6-45f171ccf496.gif)


Теперь рассмотрим поиск и бэкап. Попробуем вывести всех студентов первой группы и сохраним получившийся вывод в бэкап.

![5](https://user-images.githubusercontent.com/74643940/204664138-bb61be2c-5ae7-461b-80a2-bdc1d00df02b.gif)

Выводы:

Конечным итогом лабораторной работы стала система управления БД, написанная на языке Python и обладающая всем указанным в условии функционалом. Получен опыт работы в графической среде PyQT, а также ООП на выбранном языке. Работа загружена в репозиторий GitHub и в дальнейшем будет преподноситься в качестве pet-проекта при трудоустройстве.
