Wicket SpringSecurity Example
=============================

###Как запустить

1. mvn clean install
2. mvn jetty:run

###Зачем

Показать, что Wicket может работать вместе со Spring Security.

###Продемонстрировано

Аутентификация с захардкожеными логином-паролем, авторизация ролями, защита URL ролями, защита от Cross-Site Request Forgery, страница логина и логаута.

###Лицензия

**можно**

Я считаю, что здесь находится очевидный код, доступный для написания первокласснику, поэтому лицензии — глупость.
Формально лицензия Apache2.0, подходит для халявного использования в коммерческом проекте, подробней в LICENSE и NOTICE.
Здесь лицензия приводится из уважения к правилам Гитхаба и отсутствия возможности передать код в Public Domain другим способом.

Началось с [вот этой статьи](https://codepitbull.wordpress.com/2013/07/31/using-spring-security-3-with-wicket-6-authroles-and-javaconfig-and-a-little-servlet-3/).

Что было сделано после нее:

* добавлена сборка через Maven
* внесены изменения для совместимости с новым спрингом
* решена проблема с CSRF-проверками нового спринга, имхо очень костыльно, смотреть на init/CsrfTokenFilter
* налажен запуск из нового Jetty
* web.xml не используется, запуск через программный ApplicationInitializer
* web.xml всё еще можно использовать
* Java 8

