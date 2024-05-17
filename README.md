Permalist App
Permalist is a simple to-do list application built using Node.js, Express, and PostgreSQL. The application allows users to add, edit, and delete items from a list.

Features
Display a list of items
Add new items to the list
Edit existing items in the list
Delete items from the list
Prerequisites
Before you begin, ensure you have the following installed:

Node.js
PostgreSQL
Installation
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/permalist.git
cd permalist
Install dependencies:
bash
Copy code
npm install
Set up PostgreSQL database:
Start PostgreSQL service
Create a database named permalist
Create a table named items with the following schema:
sql
Copy code
CREATE TABLE items (
  id SERIAL PRIMARY KEY,
  title VARCHAR(255) NOT NULL
);
Configure database connection:
Open index.js and update the db connection details if necessary:
javascript
Copy code
const db = new pg.Client({
  user: "postgres",
  host: "localhost",
  database: "permalist",
  password: "YourPassword",
  port: 5432,
});
Usage
Start the server:
bash
Copy code
npm start
Open your web browser and navigate to http://localhost:3000.
API Endpoints
GET / - Display the list of items
POST /add - Add a new item
POST /edit - Edit an existing item
POST /delete - Delete an item
Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes.
