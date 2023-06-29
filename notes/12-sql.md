# SQL

<UPPERCASE IS SQL 
<lowercase is my data

>dbSetup.Sql

>CREATE TABLE ??(
  id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  name TEXT NOT NULL,
  age INT DEFAULT 1,
  species TEXT

  name VARCHAR(255) <max byte size in parenthesis
);
>execute

INSERT INTO penguins;
(name, age, species)
VALUES
("Penny", 2, Macaroni)
>execute

SELECT * FROM penguins; <grabs all info from db
SELECT name FROM penguins; <is a single data from table
SELECT name, species FROM penguins WHERE id =1  <grabs a penguin name and species data with an id of 1

>UPDATE penguins SET 
`wearingTux` = true;    <changes all bool to true
WHERE id = 4; <changes only the id 4

<DELETE FROM penguins WHERE id = 3; deletes the id 3

ENV  APP SETTINGS.JSON
DB SETUP

Foreign Key (creatorId) REFERENCES accounts(id) ON DELETE CASCADE <Constraint 

<JOIN TABLES

SELECT title, 
name 
FROM albums 
JOIN account ON creatorId = albums.creator.id;

add privateReadOnly Auth0provider to controller

<create album
async needs Task added to the Action
Account userInfo = await _auth0.GetUserInfo<Account>(HttpContext);
albumData.CreatorId = userInfo.Id;






