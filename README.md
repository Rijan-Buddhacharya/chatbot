Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/yourusername/chatbot.git
cd chatbot
Set Up the Database:

Open your MySQL/MariaDB client and create a new database:

sql
Copy code
CREATE DATABASE both;
Create a chatbot table using the following SQL command:

sql
CREATE TABLE chatbot (
    id INT AUTO_INCREMENT PRIMARY KEY,
    queries VARCHAR(255) NOT NULL,
    replies TEXT NOT NULL
);
Insert initial data into the chatbot table:

sql
INSERT INTO chatbot (queries, replies) VALUES
('hello', 'Hi there! How can I assist you?'),
('how are you', 'I am just a bot, but thanks for asking! How about you?'),
('bye', 'Goodbye! Have a great day!'),
('help', 'Sure, I am here to help. What do you need assistance with?'),
-- Add more queries and replies here
;
Configure the Database Connection:

Open message.php and update the database connection settings:

php
$conn = mysqli_connect("localhost", "newuser", "password", "both") or die("Database Error");

Start the PHP Built-in Server:

Run the following command in your terminal from the project directory:

bash
php -S localhost:8000
