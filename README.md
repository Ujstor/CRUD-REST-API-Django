# Python CRUD REST API using Django, Postgres, Docker, and Docker Compose

This project is a sample implementation of a CRUD (Create, Read, Update, and Delete) REST API using Python, Django, Postgres, Docker, and Docker Compose.

The API allows users to create, read, update, and delete records in a database table. It includes endpoints for performing these operations, as well as endpoints for retrieving a list of all records and retrieving a single record by its ID.

## Getting started

To get started with this project, you'll need to have Docker and Docker Compose installed on your system. You can download them from the official websites:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

Once you have Docker and Docker Compose installed, you can clone this repository and run the following command in the root directory of the project:

```bash
docker-compose up
```

This command will build and start the Docker containers for the Django application and the Postgres database. Once the containers are up and running, you can access the API at `http://localhost:8000/users/`.

## API endpoints

The API includes the following endpoints:

- `GET /users/`: Retrieves a list of all records.
- `GET /users/read/:id/`: Retrieves a single record by its ID.
- `POST users/create/`: Creates a new record.
- `PUT /users/update/:id/`: Updates an existing record by its ID.
- `DELETE /users/delete/:id/`: Deletes an existing record by its ID.

## Testing with Postman and TablePlus

To test the API endpoints of this project, you can use Postman, a popular API testing tool. With Postman, you can send HTTP requests to the API and see the response data in a user-friendly interface.

You can also use TablePlus, a database management tool, to interact with the Postgres database directly and see the changes made by the API.

Here's an example workflow for testing the API endpoints using Postman and TablePlus:

1. Start the Docker containers for the Django application and the Postgres database by running the following command in the root directory of the project:

```bash
docker-compose up
```

2. Open Postman and create a new request. Set the request method to `POST` and the URL to `http://localhost:8000/user/create/`.

3. In the request body, add JSON data for creating a new user. For example:

```json
{
    "name": "John",
    "email": "john.doe@example.com"
}
```

1. Send the request and check the response. If the user is created successfully, you should see a response with a `201 Created` status code and the user data in JSON format.

2. Open TablePlus and connect to the Postgres database using the following settings:

- Host: `localhost`
- Port: `5432`
- Database: `postgres`
- Username: `postgres`
- Password: `postgres`

6. Open the `users` table and refresh the view. You should see a new row with the data for the user you just created.

7. Repeat the process for the other API endpoints, such as updating and deleting users. Use Postman to send the requests and TablePlus to see the changes in the database.

By using Postman and TablePlus, you can easily test and debug the API endpoints of this project, and ensure that they are working correctly.

## Conclusion

This project provides a basic example of how to build a CRUD REST API using Python, Django, Postgres, Docker, and Docker Compose. You can use it as a starting point for building your own APIs or modify it to suit your specific needs.