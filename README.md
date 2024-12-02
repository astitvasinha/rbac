Prerequisites for the execution of the project:
(Note: This installation process is for windows system. For other OS 
steps followed below may differ)
Few things required for the execution of the project are as follows-:

a. Node JS should be installed on the system
b. Install CRA(create-react-app) on the system. Open the cmd as admin and type "npm install -g create-react-app"
c. Nodemon should be installed on the system. I have it installed it globally on my system.
Open the cmd as admin and type "npm i nodemon" to install it.
d. Install REST Client for VS Code (my IDE) to test the GET and POST request.

To start the project navigate to rbac/backend in terminal and type "nodemon index" to start the backend server.
In a new terminal, navigate to rbac/frontend and type "npm start" to load the frontend interface.

Admin credentials: email: "admin@gmail.com", password: "123456"
 
There are 2 sections for this file. The first section explains the backend and the second section explains the frontend.

Backend

Dependencies used are-:
argon2 - for password hashing (better than bcrypt)
cors - to access API outside the domain
mysql2 - mysql client
sequelize - ORM required to interact with mysql2
dotenv - to use environment variables
express - framework for building server-side application and API 
express-session - middleware for Express for the management of user-seesions
connect-session-sequelize - used to sync the session and store the current progress in database

Backend includes the database setup in mysql using phpMyAdmin, controllers to manage the products,
users and authentication of the user that is logged in. These controller files will serve as an 
intermidiaries between the database models and the visual interface, handling HTTP requests, 
processing them and returning appropriate responses. There are 2 database models used in this project.
One is for the products and second is for the users. The middleware "AuthUser.js" is secures the endpoint
between the connections.

Frontend

Dependencies used:
axios - to send asynchronous HTTP requests to REST endpoints, perform CRUD operations and handle responses
bulma - modern CSS framework based on flexbox that provides ready-to-use styles and components
react-router-dom - used to handle routings in the react application
react-redux - used to manage complex state logic and share state across components
react-icons - provides icons to use in the react application


Frontend includes the login interface. After the store there are form for adding the products, adding the user,
editing the products, editing the users. The products can be added by both admin and the user. The admin has 
permissions to create and remove users and products. The user can only add and delete the products created 
only by the user. But the admin can delete both the users and users' products.
