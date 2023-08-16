# cinenaya-postman
This collection is related to the cinema management system, here you have requests for authentication, managing cinemas, movies, reservations, and more.

Each item in the collection represents a different API request along with its associated details such as request method, headers, body, and URL. Tests are also defined for some requests to handle the responses and set environment variables. Here's a breakdown of the main components of your collection:

## Endpoints

All endpoints, including those related to authentication, need a valid token in the headers

### Authentication:

There are three different "Login" requests for different types of users (admin, regular, and owner user). Each request sends a POST request with username and password and handles the received token in the response by setting it as an environment variable.

### Cinema Management:

- "Get list of cinemas": Retrieves a list of cinemas.
- "Create a cinema": Creates a new cinema by sending a POST request with details. 
- "Update a cinema": Updates a cinema's details with a PUT request. 
- "Delete a cinema": Deletes a cinema using a DELETE request.

### Movie Management:

- "Get a list of movies in cinema": Retrieves a list of movies being shown in a particular cinema. Requires a cinema_id as a query parameter.

### Reservation Management:

- "Get available seats": Retrieves available seats for a specific movie showing. Requires a movie_showing_id as a query parameter.
- "List reservations": Retrieves a list of reservations. 
- "Create a reservation": Creates a new reservation by sending a POST request with details. 

## Environment Variables:

The collection defines one environment variable automatically after loging: "token".
Note:

The provided URL "http://127.0.0.1:8000" is the default when you start the project following the provided documentation. You would need to replace this with the actual API endpoint if you're testing on a remote server.
This collection cover a wide range of functionalities in a cinema management system, including authentication, cinema and movie management, and reservation handling. You can import this collection into Postman to perform these API requests and tests in your own environment.
