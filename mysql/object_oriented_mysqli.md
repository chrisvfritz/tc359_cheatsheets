#Object Oriented mysqli

Mysqli is an extension available through PHP that can be used to interact with a MySQL database. The mysqli extension allows interfacing through the common procedural style or using objects, which this article will focus on. Although performance differences between the two styles are negligable, some may find that objects make it easier to organize their code.

##Opening a Connection to a MySQL database

```
$mysqli = new mysqli("host", "user", "password", "database");
```

The above PHP code connects to a MySQL database using the given parameters and returns an object that we can call methods on to perform actions such as querys. In the above case we call the object ```$mysqli``` but it can be named anything and you can even have multiple database objects in a single file—with separate variable names of course.

##Checking your Connection to the Database

The following code can be used to retrieve error data from a failed connection. While it isn't strictly necesessary, it can be helpful to users and yourself to identify if there is a problem with your code or database.

```
if ($mysqli->connect_errno) {
    echo "Failed to connect to MySQL database: " . $mysqli->connect_error;
}
```

##Querying the Database

Querying the database is done by calling the query method on the mysqli object. The SQL query is passed as a parameter of the query method demonstrated below.

```
$result = $mysqli->query("SELECT * FROM `table`");
```

The results of the database query are stored in an SQL result object which we named ```$result```.

##Getting data from a result object

Our SQL results object has methods of it's own that can be used to retrieve data.

We can find out the number of rows the object contains using ```$mysqli->num_rows();```. This can be useful to find out if no rows were returned or when looping through each row using a for loop.

If we want to get data from the result we can call the fetch_assoc method on the result and the row data will be stored in an associative array—the key being the field's name.

```
$row = $result->fetch_assoc();
echo $row['data_name'];
```

Each time we fetch a row from the object, a pointer is moved and a subsequent fetch will retrieve the next row. Therefore, if we fetch each row in a while loop we can retrieve every row of data.

```
while ($row = $result->fetch_assoc()) {
	echo $row['data_name'];
}
```

##Closing the connection to the database

Closing a database connection is as simple as calling the close method on the database object as follows: 

```
$mysqli->close();
```
While it isn't necessary to close a database connection, especially at the end of a script when it will be closed automatically, it can free up server resources if you don't intend to make any more queries.

###You can find more information about the mysqli function at [php.net](http://php.net/manual/en/book.mysqli.php)