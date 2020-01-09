<!-- conection for database using mysqli for local host -->

<?php

$con = mysqli_connect("localhost","root","password","database_name");

?>	

<!-- connection by PDO -->

<?php
 	$user='root';
 	$pass='';
    $dbname='database_name';
	
    $conn = new PDO('mysql:host=localhost;dbname= database_name', $user, $pass);
	if (!$conn) {
		die("Connection failed: " . $conn->connect_error);
	}
  	$conn->setAttribute(PDO::ATTR_DEFAULT_FETCH_MODE, PDO::FETCH_ASSOC);
?>

