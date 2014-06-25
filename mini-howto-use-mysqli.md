Title: Aprendiendo a usar MySQLi
Date: 2014-04-19 10:20
Category: Web
Tags: php, web
Slug: mini-howto-use-mysqli
Author: abr4xas
Summary: Hagamos un verdadero defer a la carga del javascript
image: http://2.bp.blogspot.com/-_pEuTgi1HuY/UfjJyTBGIPI/AAAAAAAAAfQ/DwXd5-6hSMk/s1600/mysqli.png

# ¿Qué es la extensión mysqli de PHP?

La extensión mysqli, o como a veces se le conoce, la extensión de MySQL mejorada, se desarrolló para aprovechar las nuevas funcionalidades encontradas en los sistemas MySQL con versión 4.1.3 o posterior. La extensión mysqli viene incluida en las versiones PHP 5 y posteriores. 

 La extensión mysqli contiene numerosos beneficios, siendo estas las mejoras principales respecto a la extensión mysql:

 * Interfaz orientada a objetos
 * Soporte para Declaraciones Preparadas
 * Soporte para Múltiples Declaraciones
 * Soporte para Transacciones
 * Mejoradas las opciones de depuración
 * Soporte para servidor empotrado

Para saber más clic (link: http://www.php.net/manual/es/mysqli.overview.php text: aquí popup: yes)

Ahora, vamos a la practica:

# Primer paso

     // Variables para la conexion
     define('host', 'localhost');
     define('user', '');
     define('pass', '');
     define('db' , '');

     //Abriendo una nueva conexion al MySQL server
     $mysqli = new mysqli(host, user, pass, db);

     //Salida por si hay algun error en la conexion
     if ($mysqli->connect_error) {
         die('Error: ('. $mysqli->connect_errno .') '. $mysqli->connect_error);
     }     

# Segundo paso: SELECT
     // Indicamos que es lo que queremos buscar por ejemplo, el id 1 de la tabla user
     $search_id = "1";
     $query = "SELECT * FROM user WHERE id=?";
     $statement = $mysqli->prepare($query);

     //bind parameters for markers, where (s = string, i = integer, d = double,  b = blob)
     $statement->bind_param('s', $search_id);

     //execute query
     $statement->execute();

     //bind result variables
     $statement->bind_result($id, $username, $password);

     //fetch records
     while($statement->fetch()) {
        echo '$id';
        echo '$username';
        echo '$password';
     }
# Tercer paso: DELETE
     // Indicamos que es lo que queremos buscar por ejemplo, el id 1 de la tabla user
     $search_id = "1";
     $query = "DELETE FROM user WHERE id=?";
     $statement = $mysqli->prepare($query);

     //bind parameters for markers, where (s = string, i = integer, d = double,  b = blob)
     $statement->bind_param('s', $search_id);

     //execute query
     $statement->execute();

     //bind parameters for markers, where (s = string, i = integer, d = double,  b = blob)
     $statement->bind_param('s', $search_id);

     //execute query
     if ($statement->execute()){
         echo 'Eliminado';
     }else{
         die('Error:('.$mysqli->errno.')'.$mysqli->error);
     }
NOTA: Algo que me percate fue que al realizar el DELETE si le colocaba el asterisco me daba un error, quite dicho asterisco y funciono... Extraño no? :|

# Cuarto paso: insert

Este paso lo dejare pendiente porque aun, no logro entender ciertas cosas ;)

# Quinto paso: Cerrar las conexiones abiertas

     //Esto debemos incluirlo en TODOS y cada uno de las consultas que hagamos
     $statement->close();

     //Cerrando la conexion al MySQL server, debe ser incluido al final para no dejar conexiones abiertas
     mysqli_close($conexion);

Bueno, espero que les sea de utilidad :D

FUENTE: (link: http://www.sanwebe.com/2013/03/basic-php-mysqli-usage text: PHP MySqli Basic usage popup: yes)