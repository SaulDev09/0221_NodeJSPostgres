# 0221_NodeJSPostgres

********************* Instalado *********************
npm init -y
npm i express pg
npm i nodemon -D

node src/index.js
npm run dev

********************* Con Docker *********************
docker exec -it postgres-saul01 bash
psql -U postgres
\du

********************* Cambiar cadena de conexión *********************
src/controller/index.controller.js

********************* Ejecutar en postgres *********************
CREATE DATABASE firstapi;

\l

\c firstapi;

CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(40),
    email TEXT
);

INSERT INTO users (name, email)
    VALUES ('joe', 'joe@ibm.com'),
    ('ryan', 'ryan@faztweb.com');

select * from users;

********************* Métodos *********************
1. GET 	http://localhost:3000/users
2. GET 	http://localhost:3000/users/1

3. POST 	http://localhost:3000/users
Body:
{
	"name":"Saul",
	"email":"Saul@gmail.com"
}

4. PUT 	http://localhost:3000/users/3
Body:
{
	"name":"Saul B",
	"email":"SaulB@gmail.com"
}

5. DELETE 	http://localhost:3000/users/3

