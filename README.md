# my---first--app
My frist web app for render
package.json
server.js
index.html

{
  "name": "my-first-app",
  "version": "1.0.0",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "express": "^4.18.2"
  }
}
const express = require("express");
const app = express();
const PORT = process.env.PORT || 3000;

app.use(express.static(__dirname));

app.get("/", (req, res) => {
  res.sendFile(__dirname + "/index.html");
});

app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
});

<!DOCTYPE html>
<html>
<head>
  <title>My First Render App</title>
</head>
<body>
  <h1>Hello Piyush! 👋</h1>
  <p>Your first Render app is working!</p>
</body>
</html>
