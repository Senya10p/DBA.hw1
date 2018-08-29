DBA Урок 1
Домашняя работа
1. Создали в MySQL, Postgres и SQLite одинаковые базы данных:
1.1 Изучили понятие типа SERIAL в разных базах данных.

БД MySQL
1.2 Создаём таблицу books:
CREATE TABLE `books` (
  `id` SERIAL,
  `title` TEXT,
  `author` VARCHAR(100),
  `year` INT,
  `price` FLOAT
);

1.3 Создаём таблицу publishers, с информацией об издателях:
CREATE TABLE `publishers` (
  `id` SERIAL,
  `publisher` TEXT,
  `address` TEXT
);

2. Добавляем записи в таблицу books:
INSERT INTO `books`
(`title`, `author`, `year`, `price`) VALUES ('Будущее', 'Глуховский', 2013, 600);

INSERT INTO `books`
(`title`, `author`, `year`, `price`) VALUES ('Generation «П»', 'Пелевин', 1999, 720);

INSERT INTO `books`
(`title`, `author`, `year`, `price`) VALUES ('Бойцовский клую', 'Паланик', 1996, 450);

INSERT INTO `books`
(`title`, `author`, `year`, `price`) VALUES ('Колесо времени', 'Кастанеда', 1998, 370);

INSERT INTO `books`
(`title`, `author`, `year`, `price`) VALUES ('Сумерки', 'Глуховский', 2007, 330);

Добавляем записи в таблицу publishers:
INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('АСТ', 'г. Москва');

INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('Правда Севера', 'г. Архангельск');

INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('София', 'г. Киров');

INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('Эксмо', 'г. Москва');

INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('Азбука', 'г. Санкт-Петербург');

3.1 Запрос, выбирающий все книги определенного автора:
SELECT * FROM `books`
WHERE `author`= 'Глуховский';

3.2 Запрос, выбирающий все книги не более 500 рублей:
SELECT * FROM `books`
WHERE `price` <= 500;

3.3 Запрос, выбирающий заглавия книг и год издания определенного автора, отсортированные по году их издания:
SELECT `title`, `year` FROM `books`
WHERE `author`= 'Глуховский'
ORDER BY `year`;

3.4 Запрос, выбирающий имена авторов книг, вышедших в 1990-е годы:
SELECT `author` FROM `books`
WHERE `year` BETWEEN 1990 AND 1999;

//////////////////////
БД Postrgres
1.2 Создаём таблицу books:
CREATE TABLE "books" (
  "id" SERIAL,
  "title" TEXT,
  "author" VARCHAR(100),
  "year" INT,
  "price" FLOAT
);

1.3 Создаём таблицу publishers, с информацией об издателях:
CREATE TABLE "publishers" (
  "id" SERIAL,
  "publisher" TEXT,
  "address" TEXT
);

2. Добавляем записи в таблицу books:
INSERT INTO "books"
("title", "author", "year", "price") VALUES ('Будущее', 'Глуховский', 2013, 600);

INSERT INTO "books"
("title", "author", "year", "price")  VALUES ('Generation «П»', 'Пелевин', 1999, 720);

INSERT INTO "books"
("title", "author", "year", "price")  VALUES ('Бойцовский клую', 'Паланик', 1996, 450);

INSERT INTO "books"
("title", "author", "year", "price")  VALUES ('Колесо времени', 'Кастанеда', 1998, 370);

INSERT INTO "books"
("title", "author", "year", "price")  VALUES ('Сумерки', 'Глуховский', 2007, 330);

Добавляем записи в таблицу publishers:
INSERT INTO "publishers"
("publisher", "address") VALUES ('АСТ', 'г. Москва');

INSERT INTO "publishers"
("publisher", "address") VALUES ('Правда Севера', 'г. Архангельск');

INSERT INTO "publishers"
("publisher", "address") VALUES ('София', 'г. Киров');

INSERT INTO "publishers"
("publisher", "address") VALUES ('Эксмо', 'г. Москва');

INSERT INTO "publishers"
("publisher", "address") VALUES ('Азбука', 'г. Санкт-Петербург');

3.1 Запрос, выбирающий все книги определенного автора:
SELECT * FROM "books"
WHERE "author"= 'Глуховский';

3.2 Запрос, выбирающий все книги не более 500 рублей:
SELECT * FROM "books"
WHERE "price" <= 500;

3.3 Запрос, выбирающий заглавия книг и год издания определенного автора, отсортированные по году их издания:
SELECT "title", "year" FROM "books"
WHERE "author"= 'Глуховский'
ORDER BY "year";

3.4 Запрос, выбирающий имена авторов книг, вышедших в 1990-е годы:
SELECT "author" FROM "books"
WHERE "year" BETWEEN 1990 AND 1999;

////////////////////////////
БД SQLite
1.2 Создаём таблицу books:
CREATE TABLE `books` (
  `id` INTEGER PRIMARY KEY AUTOINCREMENT,
  `title` TEXT,
  `author` VARCHAR(100),
  `year` INT,
  `price` FLOAT
);

1.3 Создаём таблицу publishers, с информацией об издателях:
CREATE TABLE `publishers` (
  `id` INTEGER PRIMARY KEY AUTOINCREMENT,
  `publisher` TEXT,
  `address` TEXT
);

2. Добавляем записи в таблицу books:
INSERT INTO books
(`title`, `author`, `year`, `price`) VALUES ('Будущее', 'Глуховский', 2013, 600);

INSERT INTO `books`
(`title`, `author`, `year`, `price`) VALUES ('Generation «П»', 'Пелевин', 1999, 720);

INSERT INTO `books`
(`title`, `author`, `year`, `price`) VALUES ('Бойцовский клую', 'Паланик', 1996, 450);

INSERT INTO `books`
(`title`, `author`, `year`, `price`) VALUES ('Колесо времени', 'Кастанеда', 1998, 370);

INSERT INTO `books`
(`title`, `author`, `year`, `price`) VALUES ('Сумерки', 'Глуховский', 2007, 330);

Добавляем записи в таблицу publishers:
INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('АСТ', 'г. Москва');

INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('Правда Севера', 'г. Архангельск');

INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('София', 'г. Киров');

INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('Эксмо', 'г. Москва');

INSERT INTO `publishers`
(`publisher`, `address`) VALUES ('Азбука', 'г. Санкт-Петербург');

3.1 Запрос, выбирающий все книги определенного автора:
SELECT * FROM `books`
WHERE `author`= 'Глуховский';

3.2 Запрос, выбирающий все книги не более 500 рублей:
SELECT * FROM `books`
WHERE `price` <= 500;

3.3 Запрос, выбирающий заглавия книг и год издания определенного автора, отсортированные по году их издания:
SELECT `title`, `year` FROM `books`
WHERE `author`= 'Глуховский'
ORDER BY `year`;

3.4 Запрос, выбирающий имена авторов книг, вышедших в 1990-е годы:
SELECT `author` FROM `books`
WHERE `year` BETWEEN 1990 AND 1999;
