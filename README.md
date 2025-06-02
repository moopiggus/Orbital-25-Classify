# Orbital-25-Classify

NUS Orbital 25 Project - Classify

A website to make planning your NUS timetable and scheduling group projects more convenient.

Created by Joel and Hui En over the course of the summer break in 2025.

Set up instructions (sorry!)

Download MySQL Workbench
User: root
Password: password*
Enter the following script:
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;
CREATE DATABASE orbitalusers;
CREATE TABLE users (
id INT AUTO_INCREMENT PRIMARY KEY,
username VARCHAR(255) NOT NULL UNIQUE,
pass VARCHAR(255) NOT NULL
);
CREATE TABLE user_following (
user_id INT NOT NULL, 
followed_id INT NOT NULL,    
UNIQUE(user_id, followed_id),
FOREIGN KEY (user_id) REFERENCES users(id),
FOREIGN KEY (followed_id) REFERENCES users(id)
);
Click lightning to run

git clone https://github.com/moopiggus/Orbital-25-Classify.git 
New folder should have frontend / backend folder and gitignore and readme
Open in vscode
In vscode click terminal (at the top) > new terminal, your path directory in the terminal should be something like ..\Desktop\Classify
cd frontend 
Type into terminal:
npm install tailwindcss @tailwindcss/postcss postcss react react-dom react-router-dom react-scripts axios
cd ../backend
npm install cors mysql express bcrypt

To run: 
npm run start 


