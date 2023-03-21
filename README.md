# job4j_cars

## <p id="contents">Оглавление</p>

<ul>
<li><a href="#01">Описание проекта</a></li>
<li><a href="#02">Стек технологий</a></li>
<li><a href="#03">Требования к окружению</a></li>
<li><a href="#04">Сборка и запуск проекта</a>
    <ol type="1">
        <li><a href="#0401">Сборка проекта</a></li>
        <li><a href="#0402">Запуск проекта</a></li>
    </ol>
</li>
<li><a href="#05">Взаимодействие с приложением</a>
    <ol  type="1">
        <li><a href="#0501">Страница приветствия</a></li>
        <li><a href="#0502">Регистрация пользователя</a></li>
        <li><a href="#0503">Страница входа</a></li>
        <li><a href="#0504">Список всех объявлений</a></li>
        <li><a href="#0505">Страница объявления с подробностями</a></li>
        <li><a href="#0506">Страница "моих" объявлений</a></li>
        <li><a href="#0507">Страница создания объявления</a></li>
        <li><a href="#0508">Страница редактирования объявления</a></li>
        <li><a href="#0509">Выход из приложения</a></li>
    </ol>
</li>
<li><a href="#todo">TODO</a></li>
<li><a href="#contacts">Контакты</a></li>
</ul>

## <p id="01">Описание проекта</p>
Web приложение, площадка для размещения объявлений по продаже автомобилей.
* Регистрация пользователей, доступно редактирование профиля.
* Аутентификация и авторизация пользователей через Servlet Filter.
* Добавление, редактирование, удаление объявлений.
* Просмотр списка своих объявлений.
* Изменения статуса объявлений, перевод в категорию проданных.

<p><a href="#contents">К оглавлению</a></p>

# <p id="02">Стек технологий</p>
- Java 14
- Spring Boot 2.6
- HTML 5, HTML 5, Thymeleaf, Bootstrap 4
- Hibernate 5.4
- PostgreSql 14
- JUnit 5
- Maven 3.8

<p><a href="#contents">К оглавлению</a></p>

Инструменты:
- Javadoc, JaCoCo, Checkstyle

<p><a href="#contents">К оглавлению</a></p>

## <p id="03">Требования к окружению</p>

Java 14, Maven 3.8, PostgreSQL 14

<p><a href="#contents">К оглавлению</a></p>

## <p id="04">Сборка и запуск проекта</p>

Для выполнения действий данного раздела необходимо установить 
и настроить систему сборки проектов Maven.

По умолчании проект компилируется и собирается в директорию target.  

### <p id="0401">1. Сборка проекта</p>

Команда для сборки в war
`mvn clean package -DskipTests`

<p><a href="#contents">К оглавлению</a></p>

### <p id="0402">2. Запуск проекта</p>

Перед запуском проекта необходимо создать базу данных todo
в PostgreSQL, команда для создания базы данных:
`create database carshop;`
Средство миграции Liquibase автоматически создаст структуру
базы данных и наполнит ее предустановленными данными.
Команда для запуска
`mvn spring-boot:run`

<p><a href="#contents">К оглавлению</a></p>

## <p id="05">Взаимодействие с приложением</p>

### <p id="0501">1. Страница приветствия</p>
Со страницы приветствия пользователь может перейти к регистрации, либо к странице входа.

![alt text](images/cars_img_1.jpg)

<p><a href="#contents">К оглавлению</a></p>

### <p id="0502">2. Регистрация пользователя</p>
Каждому пользователю присваивается пара: наименование аккаунта (email) и пароль.
Помимо имени аккаунта и пароля указываются: имя пользователя и телефон, эта контактная
информация отображаются на странице объявления.

![alt text](images/cars_img_2.jpg)

<p><a href="#contents">К оглавлению</a></p>

### <p id="0503">3. Страница входа</p>
Для входа необходимо ввести пароль и электронную почту (наименование аккаунта), указанную при регистрации.

![alt text](images/cars_img_3.jpg)

<p><a href="#contents">К оглавлению</a></p>

### <p id="0504">4. Список всех объявлений</p>
На странице выводится список всех объявлений пользователей сайта.

![alt text](images/cars_img_4.jpg)

<p><a href="#contents">К оглавлению</a></p>

### <p id="0505">5. Страница объявления с подробностями</p>
На странице выводится объявление со всей доступной информацией: комментарии продавца,
контактная информация (имя, телефон).

![alt text](images/cars_img_8.jpg)

<p><a href="#contents">К оглавлению</a></p>

### <p id="0506">6. Страница "моих" объявлений</p>
На странице выводится объявления созданных пользователем приложения.
Присутствуют кнопки редактирования и удаления объявлений.

![alt text](images/cars_img_5.jpg)

<p><a href="#contents">К оглавлению</a></p>

### <p id="0507">7. Страница создания объявления</p>
На странице заполняется информация по продаваемому автомобилю, при 
необходимости загружается фотография.

![alt text](images/cars_img_6.jpg)

<p><a href="#contents">К оглавлению</a></p>

### <p id="0508">8. Страница редактирования объявления</p>
На странице редактируется информация по поданному ранее объявлению.

![alt text](images/cars_img_7.jpg)

<p><a href="#contents">К оглавлению</a></p>

### <p id="0509">9. Выход из приложения</p>

При нажатии в панели навигации на ссылку "Выход", происходит
выход пользователя из приложения с перенаправлением на страницу входа и
сообщением о том, что пользователь вышел. При выходе сессия в которой работал
пользователь удаляется.

![alt text](images/cars_img_8.jpg)

<p><a href="#contents">К оглавлению</a></p>

## <p id="todo">TODO list</p>
* Добавить в другую ветку работу с пользователями через Spring Security

<p><a href="#contents">К оглавлению</a></p>

## <p id="contacts">Контакты </p>

[![alt-text](https://img.shields.io/badge/-telegram-grey?style=flat&logo=telegram&logoColor=white)](https://t.me/T_AlexME)&nbsp;&nbsp;
[![alt-text](https://img.shields.io/badge/@%20email-005FED?style=flat&logo=mail&logoColor=white)](mailto:amemelyanov@yandex.ru)&nbsp;&nbsp;

<p><a href="#contents">К оглавлению</a></p>