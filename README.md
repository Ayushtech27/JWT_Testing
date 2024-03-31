# JWT TESTING

# Setting up

- After cloning run the command npm install

- Create a .env file with the variable PORT and assign it a desired numeric value. e.g. PORT=3000

- Run the command npm start

# Testing in postman or thunderclient

- Check if the app is running correctly using the get request endpoint "http://localhost:'your_port'/api/login"

- Faliure Case

  - Try accessing the /api/posts route without providing the token in the Authorization header. You should receive a 403 Forbidden response.(Post Request)

- Success Case
  - Set up a POST request to http://localhost:'your port'/api/login
  - Send the request and ensure you receive a response containing a JWT token. (User is hardcoaded in the code)
  - Copy the JWT token
  - Set up a POST request to http://localhost:'your_port'/api/posts
  - In the request headers, add an 'Authorization' header with the value Bearer 'token', where 'token' is the JWT token you copied in the previous step.
  - Send the request and observe the response. If the token is valid, you should receive a response with the message "POST created..." along with the authenticated user data.
