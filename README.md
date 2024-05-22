## [REST API](http://localhost:8080/doc)

## Концепция:

- Spring Modulith
    - [Spring Modulith: достигли ли мы зрелости модульности](https://habr.com/ru/post/701984/)
    - [Introducing Spring Modulith](https://spring.io/blog/2022/10/21/introducing-spring-modulith)
    - [Spring Modulith - Reference documentation](https://docs.spring.io/spring-modulith/docs/current-SNAPSHOT/reference/html/)

```
  url: jdbc:postgresql://localhost:5432/jira
  username: jira
  password: JiraRush
```

- Есть 2 общие таблицы, на которых не fk
    - _Reference_ - справочник. Связь делаем по _code_ (по id нельзя, тк id привязано к окружению-конкретной базе)
    - _UserBelong_ - привязка юзеров с типом (owner, lead, ...) к объекту (таска, проект, спринт, ...). FK вручную будем
      проверять

## Аналоги

- https://java-source.net/open-source/issue-trackers

## Тестирование

- https://habr.com/ru/articles/259055/

Список выполненных задач:
...
1. Розібратися зі структурою проєкту (onboarding). +
2. Видалити соціальні мережі: vk, yandex. +

![img.png](img.png)

3. Винести чутливу інформацію до окремого проперті файлу. +

![img_1.png](img_1.png)

4. Переробити тести так, щоб під час тестів використовувалася in memory БД (H2), а не PostgreSQL. +

![img_2.png](img_2.png)

5. Написати тести для всіх публічних методів контролера ProfileRestController. +

![img_3.png](img_3.png)

6. Зробити рефакторинг методу com.javarush.jira.bugtracking.attachment.FileUtil#upload. +