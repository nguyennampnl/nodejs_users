Ref: https://expressjs.com/en/starter/generator.html

# Install

npm install -g express-generator

# Create app

express --view=pug users


# run

```bash
nodemon app.js
```

http://localhost/
http://localhost/users

================================================================

DEBUG=users:* npm start

http://localhost:3000/

# Documents

## routing

https://expressjs.com/en/starter/basic-routing.html

### GET

app.get('/', function (req, res) {
  res.send('Hello World!')
})

### Respond to POST request on the root route (/), the application’s home page:

app.post('/', function (req, res) {
  res.send('Got a POST request')
})

### Respond to a PUT request to the /user route:

app.put('/user', function (req, res) {
  res.send('Got a PUT request at /user')
})

### Respond to a DELETE request to the /user route:

app.delete('/user', function (req, res) {
  res.send('Got a DELETE request at /user')
})

## Databases

Ref: https://expressjs.com/en/guide/database-integration.html#mysql

### MySql

#### Install
npm install mysql


#### Example

var mysql = require('mysql')
var connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: 'NguyenNam2020',
  database: 'users'
})

connection.connect()

connection.query('SELECT 1 + 1 AS solution', function (err, rows, fields) {
  if (err) throw err

  console.log('The solution is: ', rows[0].solution)
})

connection.end()



