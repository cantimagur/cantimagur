### Hi there 👋

<!--
**cantimagur/cantimagur** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->


SELECT title,description FROM film;

SELECT * FROM film
--WHERE length > 60 AND length < 75;

WHERE rental_rate = 0.99 AND replacement_cost = 12.99 OR replacement_cost = 28.99;

SELECT * FROM customer
WHERE first_name = 'Mary';

SELECT * FROM film
WHERE NOT length > 50 AND NOT (rental_rate = 2.99 OR rental_rate = 4.99);





BETWEEN IN EXERCİSE

SELECT * FROM film
WHERE replacement_cost BETWEEN 12.99 AND 16.99;

SELECT * FROM actor
WHERE first_name IN ('Penelope','Nick','Ed');

SELECT * FROM film
WHERE (rental_rate IN (0.99,2.99,4.99)) AND (replacement_cost IN (12.99,15.99,28.99));


LIKE ILIKE EXERCİSE

--SELECT * FROM country
--WHERE country LIKE 'A%a';

--SELECT country FROM country
--WHERE country LIKE '%n' AND LENGTH (country) >=6;


--SELECT * FROM film
--WHERE title LIKE 'C%' AND length > 90 AND rental_rate = 2.99 ;


DISTINCT COUNT EXERCİSE


--SELECT DISTINCT replacement_cost FROM film;

--SELECT COUNT(DISTINCT replacement_cost) FROM film;

--SELECT COUNT(*) FROM film
--WHERE title = 'T%' AND rating = 'G';

--SELECT COUNT(*) FROM country
--WHERE country LIKE '_____';

--SELECT COUNT(*) FROM city
--WHERE city ILIKE '%R';


ORDER BY / LIMIT / OFFSET EXERCİSE

SELECT * FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;


SELECT * FROM film
WHERE title LIKE '%n'
ORDER BY length ASC
OFFSET 5
LIMIT 5;

SELECT * FROM customer
WHERE store_id = 1
ORDER BY last_name DESC 
LIMIT 4;


AGGREGATE EXERCİSE

SELECT AVG(rental_rate) FROM film;
SELECT ROUND(AVG(rental_rate),2)FROM film;

SELECT COUNT(*) FROM film
WHERE title LIKE 'C%';

SELECT MAX(length) FROM film
WHERE rental_rate = 0.99;

SELECT COUNT(DISTINCT replacement_cost) FROM film
WHERE length > 150;

GROUP BY / HAVING EXERCİSE

SELECT rating, COUNT(*) FROM film
GROUP BY rating;


SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50 


SELECT store_id, COUNT(*) FROM customer
GROUP BY store_id;

SELECT country_id, COUNT(*) FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;


CREATE TABLE,UPDATE AND DELETE EXERCİSE

CREATE TABLE employee (
	id INTEGER ,
	name VARCHAR(50),
	birthday DATE,
	email VARCHAR(100)
);


insert into employee (id, Name, birthday, email) values (1, 'Ree Pook', '2021-09-13', 'rpook0@seattletimes.com');
insert into employee (id, Name, birthday, email) values (2, 'Julie Edmondson', '2020-11-26', 'jedmondson1@w3.org');
insert into employee (id, Name, birthday, email) values (3, 'Lowell Ingleston', '2021-04-18', 'lingleston2@symantec.com');
insert into employee (id, Name, birthday, email) values (4, 'Charla Hazeldean', '2021-02-10', 'chazeldean3@comsenz.com');
insert into employee (id, Name, birthday, email) values (5, 'Shane Defraine', '2021-08-30', 'sdefraine4@moonfruit.com');
insert into employee (id, Name, birthday, email) values (6, 'Conrade Botterman', '2021-08-11', 'cbotterman5@spiegel.de');
insert into employee (id, Name, birthday, email) values (7, 'Christie Ruckhard', '2020-12-31', 'cruckhard6@scribd.com');
insert into employee (id, Name, birthday, email) values (8, 'Roanna Stapylton', '2020-11-18', 'rstapylton7@google.pl');
insert into employee (id, Name, birthday, email) values (9, 'Doloritas Fittis', '2021-06-27', 'dfittis8@google.nl');
insert into employee (id, Name, birthday, email) values (10, 'Jenica Gillam', '2020-11-03', 'jgillam9@china.com.cn');
insert into employee (id, Name, birthday, email) values (11, 'Stanleigh Emanson', '2021-09-03', 'semansona@clickbank.net');
insert into employee (id, Name, birthday, email) values (12, 'Rollie Prozescky', '2021-07-11', 'rprozesckyb@arstechnica.com');
insert into employee (id, Name, birthday, email) values (13, 'Deeann Gredden', '2021-06-08', 'dgreddenc@flickr.com');
insert into employee (id, Name, birthday, email) values (14, 'Gayleen Keedy', '2020-12-26', 'gkeedyd@hc360.com');
insert into employee (id, Name, birthday, email) values (15, 'Flossi De L''Isle', '2021-08-09', 'fdee@purevolume.com');
insert into employee (id, Name, birthday, email) values (16, 'Nowell Prall', '2020-12-28', 'nprallf@ibm.com');
insert into employee (id, Name, birthday, email) values (17, 'Daren Turton', '2021-07-23', 'dturtong@nymag.com');
insert into employee (id, Name, birthday, email) values (18, 'Shena Flukes', '2021-03-16', 'sflukesh@aboutads.info');
insert into employee (id, Name, birthday, email) values (19, 'Curtis Zamora', '2020-11-16', 'czamorai@cnet.com');
insert into employee (id, Name, birthday, email) values (20, 'Hadrian Shotboult', '2021-03-04', 'hshotboultj@163.com');
insert into employee (id, Name, birthday, email) values (21, 'Vitia Snoday', '2021-09-04', 'vsnodayk@themeforest.net');
insert into employee (id, Name, birthday, email) values (22, 'Carey Reboul', '2020-10-12', 'creboull@topsy.com');
insert into employee (id, Name, birthday, email) values (23, 'Waite Parmer', '2021-03-22', 'wparmerm@netvibes.com');
insert into employee (id, Name, birthday, email) values (24, 'Hilliary Clayal', '2021-05-26', 'hclayaln@opensource.org');
insert into employee (id, Name, birthday, email) values (25, 'Aylmar Langcastle', '2021-06-20', 'alangcastleo@paypal.com');
insert into employee (id, Name, birthday, email) values (26, 'Aubine Finlow', '2021-08-25', 'afinlowp@nsw.gov.au');
insert into employee (id, Name, birthday, email) values (27, 'Hube Middleditch', '2021-04-11', 'hmiddleditchq@gmpg.org');
insert into employee (id, Name, birthday, email) values (28, 'Conny Rozec', '2021-04-08', 'crozecr@nytimes.com');
insert into employee (id, Name, birthday, email) values (29, 'Olympe Milligan', '2021-01-18', 'omilligans@marketwatch.com');
insert into employee (id, Name, birthday, email) values (30, 'Christiana Lipp', '2021-07-18', 'clippt@usda.gov');
insert into employee (id, Name, birthday, email) values (31, 'Jo Ferronel', '2021-04-26', 'jferronelu@google.ru');
insert into employee (id, Name, birthday, email) values (32, 'Martie Grew', '2021-09-03', 'mgrewv@hp.com');
insert into employee (id, Name, birthday, email) values (33, 'Darla Francioli', '2021-09-30', 'dfrancioliw@furl.net');
insert into employee (id, Name, birthday, email) values (34, 'Rip Colleton', '2021-04-29', 'rcolletonx@uiuc.edu');
insert into employee (id, Name, birthday, email) values (35, 'Nannette Lemmen', '2021-08-18', 'nlemmeny@yahoo.co.jp');
insert into employee (id, Name, birthday, email) values (36, 'Arlen Northrop', '2021-06-27', 'anorthropz@yellowpages.com');
insert into employee (id, Name, birthday, email) values (37, 'Erasmus Jorge', '2021-03-10', 'ejorge10@dot.gov');
insert into employee (id, Name, birthday, email) values (38, 'Grannie Richard', '2021-05-15', 'grichard11@dailymotion.com');
insert into employee (id, Name, birthday, email) values (39, 'Cassie Orris', '2021-07-12', 'corris12@mac.com');
insert into employee (id, Name, birthday, email) values (40, 'Maye Brekonridge', '2021-04-07', 'mbrekonridge13@yellowbook.com');
insert into employee (id, Name, birthday, email) values (41, 'Isis Casburn', '2021-04-29', 'icasburn14@google.nl');
insert into employee (id, Name, birthday, email) values (42, 'Lolita Everill', '2021-06-10', 'leverill15@cmu.edu');
insert into employee (id, Name, birthday, email) values (43, 'Jeffie Redfield', '2021-04-05', 'jredfield16@wikispaces.com');
insert into employee (id, Name, birthday, email) values (44, 'Tally Krink', '2021-09-23', 'tkrink17@dell.com');
insert into employee (id, Name, birthday, email) values (45, 'West Firmage', '2021-02-11', 'wfirmage18@paginegialle.it');
insert into employee (id, Name, birthday, email) values (46, 'Dylan Pluvier', '2021-04-12', 'dpluvier19@twitter.com');
insert into employee (id, Name, birthday, email) values (47, 'Cissy Grunson', '2021-08-21', 'cgrunson1a@wp.com');
insert into employee (id, Name, birthday, email) values (48, 'Stu Pancost', '2021-01-22', 'spancost1b@buzzfeed.com');
insert into employee (id, Name, birthday, email) values (49, 'Evan Couve', '2021-03-17', 'ecouve1c@bloglovin.com');
insert into employee (id, Name, birthday, email) values (50, 'Allianora Lancley', '2021-07-23', 'alancley1d@51.la');


DELETE FROM employee
WHERE id = 1;

SELECT * FROM employee;

UPDATE employee
SET name = 'can timağur'
WHERE id = 4;

SELECT * FROM employee
ORDER BY id ASC;

DELETE FROM employee
WHERE name = 'Julie Edmondson';

SELECT * FROM employee;

UPDATE employee
SET email = 'can.timagur@eva.guru'
WHERE id = 4;



INNER JOIN

SELECT city, country FROM country
INNER JOIN city ON city.country_id = country.country_id;


SELECT city.city, country.country FROM country
INNER JOIN city ON city.country_id = country.country_id;


SELECT payment_id, first_name, last_name FROM customer
INNER JOIN payment ON customer.customer_id = payment.customer_id; 

SELECT rental_id, first_name, last_name FROM customer
INNER JOIN rental ON rental.customer_id = customer.customer_id;
