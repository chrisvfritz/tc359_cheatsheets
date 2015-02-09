# Basics of PHP in a web environment and why it's useful

PHP is a server side scripting language that is commonly used to make dynamic and interactive websites.
One of the most popular use cases is for entering and retrieving data from MySQL or SQLite databases.

##Learning PHP is pretty straight forward here are some basics:
*
* Inside your html use **<?php** and **?>** to surround your PHP code.
* Declare variables using the **$**
* Print out to screen using **echo**
* End lines with a **;**

```
<html>
  <head>
  </head>
  <body>
    <?php  
      $var == 'Hello World!';
      echo $var;

    ?>
  </body>
</html>
```

##Connecting to a MySQL database

* You need the hostname, username, password, and database to form a connection with a server.
* By using mylsqi_query you can query a server. 
* Then mysqli_fetch_assoc will take your row from table allow you to echo each column by name.

```
<?php

$hostname = "localhost";
$username = "example";
$password = "12345";
$database = "My_Database";


$con = mysqli_connect($hostname, $username, $password, $databse);
$query = "SELECT * FROM `My_Table` WHERE `id` = '5'";

$result = mysqli_query($con, $query);

$row = mysqli_fetch_assoc($result);

echo `$row["name"]`;

?>
```