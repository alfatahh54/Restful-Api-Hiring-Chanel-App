# Restful-Api-Hiring-Chanel-App
<h1 align="center">ExpressJS - Restful-Api-Hiring-Chanel-App</h1>

Note App is a simple note application specially for backend only. Built with NodeJs using the ExpressJs Framework.
Express.js is a web application framework for Node.js. [More about Express](https://en.wikipedia.org/wiki/Express.js)
## Built With
[![Express.js](https://img.shields.io/badge/Express.js-4.x-orange.svg?style=rounded-square)](https://expressjs.com/en/starter/installing.html)
[![Node.js](https://img.shields.io/badge/Node.js-v.10.16-green.svg?style=rounded-square)](https://nodejs.org/)

## Requirements
1. <a href="https://nodejs.org/en/download/">Node Js</a>
2. Node_modules
3. <a href="https://www.getpostman.com/">Postman</a>
4. Web Server (ex. localhost)

## How to run the app ?
1. Open app's directory in CMD or Terminal
2. Type `npm install`
3. Make new file a called **.env**, set up first [here](#set-up-env-file)
4. Turn on Web Server and MySQL can using Third-party tool like xampp, etc.
5. Create a database with the name hiring_chanel, and import from .sql file in this project 
6. Open Postman desktop application or Chrome web app extension that has installed before
7. Choose HTTP Method and enter request url.(ex. localhost:3000/api/v1/engineers)
8. You can see all the end point [here](#end-point)

## Set up .env file
Open .env file on your favorite code editor, and copy paste this code below :
```
DB_HOST= 'localhost'
DB_USER= ''
DB_PASSWORD=''
DB_NAME= ''
PORT= 3000
SECRET_KEY=''
```

## End Point
**1. GET**
* `//engineers`
* `//engineers?search=lorem&sort=ASC&limit=5&page=1`
* `/note/:id` (Get note by id)
* `/companies`
* `/companies?search=lorem&sort=ASC&limit=5&page=`


**2. POST**
* `/engineer`
    * ``` { "name": "your name", "description": "your self description", "skill": "your sklill", "location:" your address", "date_of_birt": "your birhday", "showcase": "your photo", "date_created": date, "date_updated": date } ```

* `/company`
    * ``` {  "name": "your name", "logo": "your logo", "location:" your address", "description": "your self description" } ```
* `/login`
     * ``` {  "email": "email", "password": "your password" } ```
* `/register`
     * ``` {  "email": "email", "password": "your password", "role": "Engineer or Company" } ```

**3. PATCH**
* `/engineer/:id` (Update engineer by id)
   * ``` { "name": "your name", "description": "your self description", "skill": "your sklill", "location:" your address", "date_of_birt": "your birhday", "showcase": "your photo", "date_created": date, "date_updated": date } ```
* `/company/:id` (Update company by id)
   * ``` { "name": "your name", "logo": "your logo", "location:" your address", "description": "your self description" } ```

**4. DELETE**
* `/engineer/:id` (Delete note by id)
* `/company/:id` (Delete category by id)
