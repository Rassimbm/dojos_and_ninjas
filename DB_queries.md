1- Create 3 new dojos:
INSERT INTO dojos (name) VALUES ("Chicago"),("NYC"),("Seattle");

2- Delete the 3 dojos you just created:
DELETE FROM dojos WHERE id IN (SELECT id FROM dojos LIMIT 3);

3- Create 3 more dojos:
INSERT INTO dojos (name) VALUES ("Chicago"),("NYC"),("Seattle");

4- Create 3 ninjas that belong to the first dojo:
INSERT INTO ninjas (first_name, last_name, age, dojo_id) VALUES ("Jesse","Pinkman", 28, 4), ("Jin","Sakai", 26, 4), ("Vitorio","Scaletta", 30, 4);

5- Create 3 ninjas that belong to the second dojo:
INSERT INTO ninjas (first_name, last_name, age, dojo_id) VALUES ("Brahim","Sankaji", 31, 5), ("Zaky","Techa", 35, 5), ("Didine","Pangla", 38, 5);

6- Create 3 ninjas that belong to the last dojo:
INSERT INTO ninjas (first_name, last_name, age, dojo_id) VALUES ("Maza","Mohammed", 45, 6), ("Rassim","Techa", 35, 6), ("Mike","Leed", 33, 6);

7- Retrieve all the ninjas from the first dojo:
SELECT name FROM dojos LEFT JOIN ninjas ON dojos.id = ninjas.dojo_id WHERE (SELECT dojos.id FROM dojos ORDER BY id ASc LIMIT 1);

8- Retrieve all the ninjas from the last dojo:
SELECT * FROM dojos LEFT JOIN ninjas ON dojos.id = ninjas.dojo_id WHERE dojos.id = (SELECT dojo_id FROM ninjas ORDER BY dojo_id DESC LIMIT 1);

9- Retrieve the last ninja's dojo:
SELECT * FROM dojos WHERE dojos.id = (SELECT dojo_id FROM ninjas ORDER BY dojo_id DESC LIMIT 1);

10- Use a JOIN to retrieve the ninja with id 6 as well as the data from its dojo. Be sure to do this in one query using a join statement:
SELECT * FROM ninjas JOIN dojos ON ninjas.dojo_id = dojos.id WHERE ninjas.id = 6;

