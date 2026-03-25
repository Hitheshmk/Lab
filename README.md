<?php
$servername = "localhost";
$username = "root";
$password = ""; // Use your MySQL password
$conn = new mysqli($servername, $username, $password);
if ($conn->connect_error) {
 die("Connection failed: " . $conn->connect_error);
}
$sql = "CREATE DATABASE yuvaraja_db";
if ($conn->query($sql) === TRUE) {
 echo "Database created successfully!";
} else {
 echo "Error creating database: " . $conn->error;
}
$conn->close();
?>


<?php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "yuvaraja_db";
$conn = new mysqli($servername, $username, $password, $dbname);
if ($conn->connect_error) {
 die("Connection failed: " . $conn->connect_error);
}
$sql = "CREATE TABLE students (
 id INT AUTO_INCREMENT PRIMARY KEY,
 name VARCHAR(50),
 course VARCHAR(50),
 marks INT
)";
if ($conn->query($sql) === TRUE) {
 echo "Table created successfully <br>";
} else {
 echo "Error creating table: " . $conn->error;
}
$sql2 = "INSERT INTO students (name, course, marks)
 VALUES ('Virat', 'BCA', 95)";
if ($conn->query($sql2) === TRUE) {
 echo "Record inserted successfully";
} else {
 echo "Error inserting record: " . $conn->error;
}
$conn->close();
?>



