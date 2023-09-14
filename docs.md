# User API Endpoints Documentation

This documentation provides information about the available API endpoints for managing users using the User API. These endpoints allow you to perform various user-related operations, including user creation, retrieval, update, and deletion.

## Base URL

The base URL for accessing the User API is `https://hngbetask2.onrender.com/api/v1`

## User Data Format (UserDTO)

The User API uses JSON format for request and response data. The User Data Transfer Object (UserDTO) represents the format of user data.

```json
{
  "name": "John Doe"
}
```

## Endpoints

### 1. Create a User

- **Endpoint:** `POST https://hngbetask2.onrender.com/api/v1`
- **Description:** Creates a new user with the provided user data i.e name.
- **Request Format:** JSON UserDTO.
- **Example Request:**

  ```http
  POST /api/v1
  Content-Type: application/json

  {
    "name": "Alice Smith",

  }
  ```

- **Success Response:** HTTP 201 Created

  - **Example Response:**

    ```json
    {
      "_id": "5656576565",
      "name": "Alice Smith",
      "createdAt": "timestamp",
      "updatedAt": "timestamp"
    }
    ```

### 2. Get User by ID

- **Endpoint:** `https://hngbetask2.onrender.com/api/v1/:user_id`
- **Description:** Retrieves user details by their unique ID.
- **Parameters:** `:id` (User ID)
- **Example Request:**

  ```http
  GET https://hngbetask2.onrender.com/api/v1/:user_id
  ```

- **Success Response:** HTTP 200 OK

  - **Example Response:**

    ```json
    {
      "_id": "7878678688",
      "name": "Alice Smith",

      "createdAt": "timestamp",
      "updatedAt": "timestamp"
    }
    ```

### 3. Update User by ID

- **Endpoint:** `PUT https://hngbetask2.onrender.com/api/v1/:user_id`
- **Description:** Updates user information by their unique ID.
- **Parameters:** `:id` (User ID)
- **Request Format:** JSON UserDTO with the updated user data.
- **Example Request:**

  ```http
  PUT /api/users/user_id
  Content-Type: application/json

  {
    "name": "Updated Name"
  }
  ```

- **Success Response:** HTTP 200 OK

  - **Example Response:**

    ```json
    {
      "_id": "7878787688",
      "name": "Updated Name",

      "createdAt": "timestamp",
      "updatedAt": "timestamp"
    }
    ```

### 4. Delete User by ID

- **Endpoint:** `DELETE https://hngbetask2.onrender.com/api/v1/:user_id`
- **Description:** Deletes a user by their unique ID.
- **Parameters:** `:id` (User ID)
- **Example Request:**

  ```http
  DELETE /api/users/user_id
  ```

- **Success Response:** HTTP 204 No Content

## Error Handling

In case of errors, the API returns a custom error handler:
.

## Conclusion

This documentation covers the available API endpoints for the User API, including their descriptions, request formats, and example responses. It is essential to follow the specified request formats and handle error responses appropriately when using these endpoints in your applications.
