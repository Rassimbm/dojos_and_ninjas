1- Create 3 new dojos:
INSERT INTO dojos (name) VALUES ("Chicago"),("NYC"),("Seattle");

2- Delete the 3 dojos you just created:
DELETE FROM dojos WHERE id IN (SELECT id FROM dojos LIMIT 3);

3- Create 3 more dojos:
INSERT INTO dojos (name) VALUES ("Chicago"),("NYC"),("Seattle");

4- Create 3 ninjas that belong to the first dojo:
INSERT INTO ninjas (first_name, last_name, age, dojo_id) VALUES ("Jesse","Pinkman", 28, 4), ("Jin","Sakai", 26, 4), ("Vitorio","Scaletta", 30, 4);

