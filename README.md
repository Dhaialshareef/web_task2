# web_task2

Control Panel for Robot Movement
This project is a simple web application that allows users to control a robot by sending direction commands (forward, backward, left, right, stop) to a server. The commands are stored in a MySQL database and can be viewed on a confirmation page.

Prerequisites
Before you begin, ensure you have met the following requirements:

PHP and MySQL installed on your local machine.
A web server running  XAMPP
Access to phpMyAdmin to manage your MySQL database.
Installation
Clone the repository from GitHub.

Navigate to the project directory on your local machine.

Set up the MySQL database:

Open phpMyAdmin and create a new database named robot_control.
Create a table named directions with the following columns:
id: INT AUTO_INCREMENT PRIMARY KEY
direction: VARCHAR(255)
timestamp: TIMESTAMP (defaults to current time)
Configure the database connection:

Update the database connection details in the save_direction.php file to match your local MySQL configuration.
Run the application:

Place the project files in your web server's root directory (e.g., htdocs for XAMPP).
Open a web browser and navigate to http://localhost/<project_folder>/index.html.
Usage
Control Panel (index.html):

The control panel allows you to send commands to the server. Each button (Forward, Backward, Left, Right, Stop) will send a corresponding direction command to the server using a GET request.
The button clicks trigger the moveRobot() function, which sends a request to the save_direction.php file.
Save Direction (save_direction.php):

The save_direction.php file receives the direction command sent from the control panel and stores it in the directions table in the database.
Get Last Direction (get_last_direction.php):

The get_last_direction.php file retrieves the last direction stored in the database and displays it.
Command Confirmation:

After sending a command, you will be able to check the confirmation page or view the last direction by visiting get_last_direction.php.
Project Structure
index.html: The main control panel page where users can send movement commands to the server.
save_direction.php: This script saves the direction command sent by the control panel to the database.
get_last_direction.php: This script retrieves and displays the last direction command stored in the database.

Screenshots
![Image](https://github.com/user-attachments/assets/d8e22223-f39b-4c1c-ba9f-9063342103bb)
![Image](https://github.com/user-attachments/assets/434b2e27-d9be-4ebe-b97c-c147b6900e42)
