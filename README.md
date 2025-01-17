# PROJECT : USER AUTHENTICATION SYSTEM

# Description
HTTP-server written in Node.js using Express.js framework doing authorisation and authentication using Zod library with connection to a MongoDB

# How to run locally
1. Clone the repo
2. Install Node modules in your directory to install Node locally using command :-    
```npm install```
3. Install these libraries - Express, Zod, Mongoose, JWT token using command :-     
```npm install express```     
```npm install zod```    
```npm install mongoose```  
```npm install jsonwebtoken```  
4. You can use both Developer Tools present in your borwser and POSTMAN app for testing locally
5. For the sake of simplicity we will be looking by the process of using POSTMAN
6. Download POSTMAN in your machine and connect your MongoDB account and paste the connection string in place of config.mongodbURL (please don't forget to put them in double quotes!)
7. Turn your backend on by running the command :-    
``` node index.js```
9. Now, send a GET request through "/sign-up" route to the specified port and in body send the user details(username, password, email and age) in an object 
10. Ensure you meet the required input constraints otherwise you will get a response "Invalid input"
11. Constraints :- username - has to be unique other you will get response saying "User already exists"
password - has to be a string with minimium length of 8 characters
email - has to be a string and has to meet the basic syntax of an email id
age - has to be an integer
12. After sending the correct input you will get back a JWT toke, you can use this to sign in again
13. Send a post request with the JWT token and password in headers and if it is correct you will get a response saying "logged in"
14. Thus you can be signed in by the only unique JWT token given to you after creating an account and otherwise not
