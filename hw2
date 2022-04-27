# MYSQL
HOMEWORK2
-- Практическое задание по теме “Управление БД”
-- 1. Установите СУБД MySQL. Создайте в домашней директории файл .my.cnf, задав в нем логин и пароль, который указывался при установке.
[mysql]
user=root
password=

/*
Сначала выдавал ошибку и отказывал в доступе, но потом вроде я добился того, чтобы он запустился. пришлось добавить в корневую папку отдельно. 
*/

-- 2. Сздайте базу данных example, разместите в ней таблицу users, состоящую из двух столбцов, числового id и строкового name.
CREATE DATABASE example;
CREATE DATABASE sample;
USE example;
DROP TABLE IF EXISTS users;
CREATE TABLE users (
id SERIAL PRIMARY KEY,
name VARCHAR(255) COMMENT 'Имя пользователя');
exit

-- 3. Создайте дамп базы данных example из предыдущего задания, разверните содержимое дампа в новую базу данных sample.
mysqldump -u root -p example > sample.sql
mysql -u root -p sample < sample.sql  
mysql -u root -p
SHOW DATABASES;
DESCRIBE sample.users;
Screenshot https://prnt.sc/pg19MymAy_89

-- 4. (по желанию) Ознакомьтесь более подробно с документацией утилиты mysqldump. Создайте дамп единственной таблицы help_keyword 
    базы данных mysql. Причем добейтесь того, чтобы дамп содержал только первые 100 строк таблицы.
mysqldump -u root -p --where="1 limit 100" mysql help_keyword > first_100_rows_help_keyword.sql

Screenshot https://prnt.sc/XghhG9C7fdGa

-- Пробовал в новую БД импортировать это, не получилось, выдавало ошибку, что таблица зарезервирована базой mysql.
