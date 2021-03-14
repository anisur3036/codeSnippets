## Database Connection

- Microsoft SQL Server Database Connection

```php
    // create a database connection
    function makeConnection($server, $database, $user, $pass) 
    {
        try {
            return new PDO( "sqlsrv:server=" . $server . ";Database=" . $database . ";ConnectionPooling=0", $user, $pass);
        } catch (PDOException $e) {
            echo "DataBase Error: ".$e->getMessage();
        }
    }
```

- MYSQL Database Connection

```php
    // create a database connection
    function makeConnection($server, $database, $user, $pass) 
    {
        try {
            return new PDO( "mysql:host=$servername;dbname=" . $database, $user, $pass);
        } catch (PDOException $e) {
            echo "DataBase Error: ".$e->getMessage();
        }
    }
```