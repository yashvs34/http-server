# PROJECT : USER AUTHENTICATION SYSTEM

# Description
HTTP-server written in Node.js using Express.js framework doing authorisation and authentication using Zod library with connection to a MongoDB

# How to run locally
1. Clone the repo and install Node modules in same directory to install and use Node locally using command :- 
```npm install```  

2. Install these libraries - Express, Zod, Mongoose, JWT token using command :- 
```npm install express```
```npm install zod```
```npm install mongoose```
```npm install jsonwebtoken```  

3. You can use both Developer Tools present in your browser and POSTMAN app for testing locally  

4. We will be looking through the process of using POSTMAN  

5. Download POSTMAN in your machine and connect your MongoDB account and paste the unique connection string in place of config.mongodbURL (please don't forget to put them in double quotes!)

6. Now, send a GET request through "/sign-up" route to the specified port and in body send the user details(username, password, email and age) in an object   

7. Ensure you meet these constraints on input:-   
username - has to be unique other you will get response saying "User already exists"  
password - has to be a string with minimium length of 8 characters  
email - has to be a string and has to meet the basic syntax of an email id  
age - has to be an integer  

8. After sending the correct input you will get back a JWT token, which you can use to sign in  

9. Send a POST request with the JWT token and password in authorisation and password fields in headers and if it is correct you will get a response saying "logged in"  

10. Thus you can be signed in by the only unique JWT token given to you after creating an account and otherwise not