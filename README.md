# nodejs-simple-web-crud

## Basic
Tech stack: nodejs, express, jade, mongodb.

Part 1 is a simple page containg a userlist with create and read function.
<br/>
Part 2 is a more advanced version with CRUD function.

This project is based on the nodejs [tutorial-1](http://cwbuecheler.com/web/tutorials/2013/node-express-mongo/) and [tutorial-2](http://cwbuecheler.com/web/tutorials/2014/restful-web-app-node-express-mongodb/) written by [Christopher](http://cwbuecheler.com/) Buecheler. It's a product of learn by doing and hopefully it can serve as a good reference for nodejs and web development.

## Run instruction
- clone the project
- update express
  - `npm update -g express`
  - `npm update -g express-generator`
- check package.json and update the dependencies
  - `npm install`
- db config
  - create database data folder
    - `mkdir [data-folder-name]`
  - start db instance
    - `mongod --dbpath [path-to-data-folder]`
  - start db console
    - `mongo`
  - switch database
    - `use [your-db-name]`
    - part1 use `nodetest1` and part2 use `nodetest2`, can be modified in app.js
  - insert data (optional)
    - `db.[object-name].insert({'[attribute1]':'[value]', '[attribute2]':'[value]', ...})`
    - you can also add data from the ui after the web is up and running
    - here in this project the object-name is `usercollection`, you can use `db.usercollection.find().pretty()` to check its value
- start the web application
  - `npm start`
- access the website
  - `localhost:3000`

## File Structure
- `app.js` -> configuration
- `package.json` -> dependency management
- `view` -> web pages
- `router` -> controller
- `public` -> resources(image, js, css)
