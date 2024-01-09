1- Create 3 new dojos:
INSERT INTO dojos (name) VALUES ("Chicago"),("NYC"),("Seattle");

2- Delete the 3 dojos you just created:
DELETE FROM dojos WHERE id IN (SELECT id FROM dojos LIMIT 3);

3- Create 3 more dojos:
INSERT INTO dojos (name) VALUES ("Chicago"),("NYC"),("Seattle");

