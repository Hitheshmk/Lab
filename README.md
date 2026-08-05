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


#include <graphics.h>
#include <conio.h>

int main()
{
    int gd = DETECT, gm;
    initgraph(&gd, &gm, "");

    line(50,50,200,50);
    rectangle(50,80,200,150);
    circle(125,250,50);
    ellipse(350,250,0,360,80,40);
    arc(350,100,0,180,50);

    line(300,300,400,300);
    line(300,300,350,220);
    line(350,220,400,300);

    putpixel(450,350,WHITE);

    getch();
    closegraph();
    return 0;
}


