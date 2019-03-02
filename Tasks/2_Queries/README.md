# Задания 2

SQL - язык, в котором один и тот же запрос можно выполнить множеством способов. Поэтому довольно часто будет встречаться задание, когда надо выполнить один запрос несколькими способами.

Можно писать запросы с входным параметром, который задаётся пользователем:

```sql
Select *
from students
where n_group = :n_group
```

Появится окно с возможностью ввода значения, которое будет использовано в запросе.

## Однотабличные запросы

1. Вывести несколькими способами все имена и фамилии студентов, средний балл которых от 3 до 4.
2. Вывести несколькими способами всех студентов заданного курса
3. Познакомиться с функцией [to_char](../../Theory/6_Functions). При помощи неё вывести студентов, которые родились в 21 веке
4. Аналогично п.3 вывести всех студентов, которые родились в заданном месяце
5. Познакомиться с функцией [sysdate](../../Theory/6_Functions). Вывести всех студентов, которые родились в текущем месяце
6. Вывести всех студентов и отсортировать по номеру группы
7. Вывести всех студентов и отсортировать по номеру группы, внутри каждой группы отсортировать по фамилии от а до я
8. Вывести студентов, средний балл которых больше 4 и отсортировать по баллу от большего к меньшему
9. Из запроса №8 вывести несколькими способами на экран [только 5 студентов](../../Theory/5_Queries/README.md#однострочные-вложенные-подзапросы) с максимальным баллом
10. Выведите хобби и с использованием [условного оператора](../../Theory/6_Functions) сделайте риск словами:

    - \>=8 - очень высокий
    - \>=6 & <8 - высокий
    - \>=4 & <8 - средний
    - \>=2 & <4 - низкий
    - <2 - очень низкий

У нас появилась задача искать студентов по городу проживания. Какие способы решения этой проблемы есть? Подумайте и предложите своё решение.

## Групповые функции

[Подробнее](../../Theory/5_Queries/README.md)

1. Выведите на экран номера групп и количество студентов, обучающихся в них
2. Выведите на экран для каждой группы максимальный средний балл
3. Подсчитать количество студентов с каждой фамилией
4. Подсчитать студентов, которые родились в каждом году
5. Для студентов каждого курса подсчитать средний балл
6. Для студентов заданного курса вывести один номер групп с максимальным средним баллом
7. Для каждой группы подсчитать средний балл, вывести на экран только те номера групп и их средний балл, в которых он менее или равен 3.5. Отсортировать по от меньшего среднего балла к большему.
8. Вывести 3 хобби с максимальным риском
9. Для каждой группы в одном запросе вывести количество студентов, максимальный балл в группе, средний балл в группе, минимальный балл в группе
10. Вывести студента/ов, который/ые имеют наибольший балл в заданной группе
11. Аналогично 10 заданию, но вывести в одном запросе для каждой группы студента с максимальным баллом.

## Многотабличные запросы

[Подробнее](../../Theory/5_Queries/README.md#запросы-с-использованием-нескольких-таблиц)

1. Вывести все имена и фамилии студентов, и название хобби, которым занимается этот студент.
2. Вывести информацию о студенте, занимающимся хобби самое продолжительное время.
3. Вывести имя, фамилию, номер зачетки и дату рождения для студентов, средний балл которых выше среднего, а риск всех хобби, которыми он занимается в данный момент больше 0.9.
4. Вывести фамилию, имя, зачетку, дату рождения, название хобби и длительность в месяцах, для всех завершенных хобби.
5. Вывести фамилию, имя, зачетку, дату рождения студентов, которым исполнилось N полных лет на текущую дату, и которые имеют более 1 действующего хобби.
6. Найти средний балл в каждой группе, учитывая только баллы студентов, которые имеют хотя бы одно действующее хобби.
7. Найти название, риск, длительность в месяцах самого продолжительного хобби из действующих, указав номер зачетки студента и номер его группы.
8. Найти все хобби, которыми увлекаются студенты, имеющие максимальный балл.
9. Найти все действующие хобби, которыми увлекаются троечники 2-го курса.
10. Найти номера курсов, на которых студенты имеют в среднем более одного действующего хобби.
11. Вывести номера групп, в которых не менее 60% студентов имеют балл не ниже 4.
12. Для каждого курса подсчитать количество различных действующих хобби на курсе.
13. Вывести номер зачётки, фамилию и имя, дату рождения и номер курса для всех отличников, не имеющих хобби. Отсортировать данные по возрастанию в пределах курса по убыванию даты рождения.
14. Создать представление, в котором отображается вся информация о студентах, которые продолжают заниматься хобби в данный момент и занимаются им как минимум 5 лет.
15. Для каждого хобби вывести количество людей, которые им занимаются.
16. Вывести ИД самого популярного хобби.
17. Вывести всю информацию о студентах, занимающихся самым популярным хобби.
18. Вывести ИД 3х хобби с максимальным риском.
19. Вывести 10 студентов, которые занимаются одним (или несколькими) хобби самое продолжительно время.
20. Вывести номера групп (без повторений), в которых учатся студенты из предыдущего запроса.
21. Создать представление, которое выводит номер зачетки, имя и фамилию студентов, отсортированных по убыванию среднего балла.
22. Представление: найти каждое популярное хобби на каждом курсе.
23. Представление: найти хобби с максимальным риском среди самых популярных хобби на 2 курсе.
24. Представление: для каждого курса подсчитать количество студентов на курсе и количество отличников.
25. Представление: самое популярное хобби среди всех студентов.
26. Создать обновляемое представление.
27. Для каждой буквы алфавита из имени найти максимальный, средний и минимальный балл. (Т.е. среди всех студентов, чьё имя начинается на А (Алексей, Алина, Артур, Анджела) найти то, что указано в задании. Вывести на экран тех, максимальный балл которых больше 3.6
28. Для каждой фамилии на курсе вывести максимальный и минимальный средний балл. (Например, в университете учатся 4 Иванова (1-2-3-4). 1-2-3 учатся на 2 курсе и имеют средний балл 4.1, 4, 3.8 соответственно, а 4 Иванов учится на 3 курсе и имеет балл 4.5. На экране должно быть следующее:
    2 Иванов 4.1 3.8
    3 Иванов 4.5 4.5
29. Для каждого года рождения подсчитать количество хобби, которыми занимаются или занимались студенты.
30. Для каждой буквы алфавита в имени найти максимальный и минимальный риск хобби.
31. Для каждого месяца из даты рождения вывести средний балл студентов, которые занимаются хобби с названием «Футбол»
32. Вывести информацию о студентах, которые занимались или занимаются хотя бы 1 хобби в следующем формате: Имя: Иван, фамилия: Иванов, группа: 1234
33. Найдите в фамилии в каком по счёту символа встречается «ов». Если 0 (т.е. не встречается, то выведите на экран «не найдено».
34. Дополните фамилию справа символом # до 10 символов.
35. При помощи функции удалите все символы # из предыдущего запроса.
36. Выведите на экран сколько дней в апреле 2018 года.
37. Выведите на экран какого числа будет ближайшая суббота.
38. Выведите на экран век, а также какая сейчас неделя года и день года.
39. Выведите всех студентов, которые занимались или занимаются хотя бы 1 хобби. Выведите на экран Имя, Фамилию, Названию хобби, а также надпись «занимается», если студент продолжает заниматься хобби в данный момент или «закончил», если уже не занимает.
40. Для каждой группы вывести сколько студентов учится на 5,4,3,2. Использовать обычное математическое округление. Итоговый результат должен выглядеть примерно в таком виде:

    | SCORE | 2222 | 3011 | 4011 | 4032 |
    | ----- | ---- | ---- | ---- | ---- |
    | 2     | 0    | 0    | 0    | 1    |
    | 3     | 1    | 2    | 1    | 1    |
    | 4     | 4    | 3    | 3    | 3    |
    | 5     | 1    | 1    | 1    | 0    |

## Разное

1. Вывести ФИО и ранк студентов в зависимости от их среднего балла. Если существует 2 и более студентов с одинаковым баллом, то они должны идти под одинаковым номером. Сделать 2 варианта решения:
   - Без пропусков номеров (не важно сколько студентов имеют одинаковый балл, следующий студент с отличающимся баллом будет иметь следующий ранк (6 студентов с одинаковы баллом и ранком - 6, следующий студент ранк 7))
   - С пропуском номеров (если 3 студента 6 номер, то следующий должен быть иметь 9 ранк)

Пример вывода результата для 1 варианта:

| NAME      | SURNAME     | AVERAGE_SCORE | RANK |
| --------- | ----------- | ------------- | ---- |
| Татьяна   | Акимова     | 4.98          | 1    |
| Шарлотта  | Калла       | 4.67          | 2    |
| Виктория  | Воронцов    | 4.63          | 3    |
| Ульяна    | Кайшева     | 4.37          | 4    |
| Анастасия | Овсянникова | 4.25          | 5    |
| Виктория  | Николаева   | 4.23          | 6    |
| Нуль      | Нулёвый     | 4.23          | 6    |
| Николай   | Борисов     | 4.22          | 7    |
| Артём     | Иван        | 4.03          | 8    |
| Иван      | Иванов      | 4.02          | 9    |

2. Существует таблица заказов и таблица пользователей. Client_id & Driver_id внешние ключи на Users_id в таблице пользователей. Статус может принимать следующие значени: `('completed', 'cancelled_by_driver', 'cancelled_by_client')`. Атрибут Role может принимать значение: `('client', 'driver', 'partner')`. **Задание:** напишите запрос, который позволяет найти коэффициент отмены запросов незабаненными пользователями в заданный период 1 октября 2013 и 3 октября 2013. Запрос должен вернуть следующий результат для готовых данных (данные в таблице - не единственный вариант проверки написанного кода, будьте внимательнее. Главное правильно решить задачу, а не вывести правильный результа):

   | Day        | Cancellation Rate |
   | ---------- | ----------------- |
   | 2013-10-01 | 0.33              |
   | 2013-10-02 | 0.00              |
   | 2013-10-03 | 0.50              |

   Скрипт создания таблиц и добавления данных:

   ```sql
   CREATE TABLE  "USERS"
   ("USERS_ID" NUMBER,
   "BANNED" VARCHAR2(50),
   "ROLE" VARCHAR2(200),
   CONSTRAINT "USERS_CHECK_ROL" CHECK ( "ROLE" in ('client', 'driver','partner')) ENABLE,
   CONSTRAINT "USERS_CON" PRIMARY KEY ("USERS_ID")
   USING INDEX  ENABLE
   )
   /
   CREATE TABLE  "TRIPS"
   ("ID" NUMBER,
   "CLIENT_ID" NUMBER,
   "DRIVER_ID" NUMBER,
   "CITY_ID" NUMBER,
   "STATUS" VARCHAR2(200),
   "REQUEST_AT" VARCHAR2(50),
   CONSTRAINT "TRIPS_CHECK_CON" CHECK ( "STATUS" in ('completed', 'cancelled_by_driver', 'cancelled_by_client')) ENABLE,
   CONSTRAINT "TRIPS_CON" PRIMARY KEY ("ID")
   USING INDEX  ENABLE
   )
   /
   ALTER TABLE  "TRIPS" ADD CONSTRAINT "TRIPS_FK1" FOREIGN KEY ("CLIENT_ID")
       REFERENCES  "USERS" ("USERS_ID") ENABLE
   /
   ALTER TABLE  "TRIPS" ADD CONSTRAINT "TRIPS_FK2" FOREIGN KEY ("DRIVER_ID")
       REFERENCES  "USERS" ("USERS_ID") ENABLE
   /
   insert into Users (Users_Id, Banned, Role) values ('1', 'No', 'client');
   insert into Users (Users_Id, Banned, Role) values ('2', 'Yes', 'client');
   insert into Users (Users_Id, Banned, Role) values ('3', 'No', 'client');
   insert into Users (Users_Id, Banned, Role) values ('4', 'No', 'client');
   insert into Users (Users_Id, Banned, Role) values ('10', 'No', 'driver');
   insert into Users (Users_Id, Banned, Role) values ('11', 'No', 'driver');
   insert into Users (Users_Id, Banned, Role) values ('12', 'No', 'driver');
   insert into Users (Users_Id, Banned, Role) values ('13', 'No', 'driver');
    insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('1', '1', '10', '1', 'completed', '2013-10-01');
   insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('2', '2', '11', '1', 'cancelled_by_driver', '2013-10-01');
   insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('3', '3', '12', '6', 'completed', '2013-10-01');
   insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('4', '4', '13', '6', 'cancelled_by_client', '2013-10-01');
   insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('5', '1', '10', '1', 'completed', '2013-10-02');
   insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('6', '2', '11', '6', 'completed', '2013-10-02');
   insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('7', '3', '12', '6', 'completed', '2013-10-02');
   insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('8', '2', '12', '12', 'completed', '2013-10-03');
   insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('9', '3', '10', '12', 'completed', '2013-10-03');
   insert into Trips (Id, Client_Id, Driver_Id, City_Id, Status, Request_at) values ('10', '4', '13', '12', 'cancelled_by_driver', '2013-10-03');
   ```