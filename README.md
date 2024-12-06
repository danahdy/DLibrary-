# Library Management API

This project is a straightforward API built with PHP and the Slim framework and Firebase, designed to manage library resources. It includes functionality for user authentication, author and book management, and handles token-based authentication using JSON Web Tokens (JWT).

## Features

- **User Management**: Includes functions for registration, authentication, viewing, updating, and deleting user profiles.
- **Author Management**: Allows adding, displaying, updating, and removing authors.
- **Book Management**: Facilitates registering, displaying, updating, and deleting books.
- **Book-Author Management**: Manages the relationship between books and authors, including the addition, modification, and removal of associations.
- **Token Management**: Supports token generation, validation, revocation, and deletion.

## How to use?

### User Management

- **Create User**  
  Endpoint: `/user/register`  
  Method: `POST`  
  Payload:  
  ```
  {
    "username": "your_username",
    "password": "your_password"
  }
  
- **Authenticate User**  
  Endpoint: `/user/auth`  
  Method: `POST`  
  Payload:  
  ```
  {
    "username": "your_username",
    "password": "your_password"
  }

  - **Show User**  
  Endpoint: `/user/show`  
  Method: `GET`  
  Payload:  
  ```
{
  "Authorization": "Bearer your_token"
}

  - **Update User**  
  Endpoint: `/user/update`  
  Method: `PUT`  
  Payload:  
  ```
{
  "token": "your_token",
  "userid": "your_userid",
  "username": "your_new_username",
  "password": "your_new_password"
}

  - **Delete User**  
  Endpoint: `/user/update`  
  Method: `DELETE`  
  Payload:  
  ```
{
  "token": "your_token",
  "userid": "your_userid"
}

### Author Management

- **Register Author**  
  Endpoint: `/author/register`  
  Method: `POST`  
  Payload:  
  ```
  {
  "token": "your_token",
  "name": "author_name"
  }

  - **Show Author**  
  Endpoint: `/author/show`  
  Method: `GET`  
  Payload:  
  ```
{
  "Authorization": "Bearer your_token"
}

  - **Update Author**  
  Endpoint: `/author/update`  
  Method: `PUT`  
  Payload:  
  ```
{
  "token": "your_token",
  "authorid": "author_id",
  "name": "author_name"
}

  - **Delete Author**  
  Endpoint: `/author/update`  
  Method: `DELETE`  
  Payload:  
  ```
{
  "token": "your_token",
  "authorid": "author_id"
}

### Book Management

- **Register Book**  
  Endpoint: `/book/register`  
  Method: `POST`  
  Payload:  
  ```
  {
  "token": "your_jwt_token",
  "title": "book_title",
  "authorid": 1
  }

  - **Show Book**  
  Endpoint: `/book/show`  
  Method: `GET`  
  Payload:  
  ```
{
  "Authorization": "Bearer your_token"
}

  - **Update Book**  
  Endpoint: `/book/update`  
  Method: `PUT`  
  Payload:  
  ```
{
  "token": "your_jwt_token",
  "bookid": 1,
  "title": "new_book_title",
  "authorid": 1
}

  - **Delete Book**  
  Endpoint: `/book/update`  
  Method: `DELETE`  
  Payload:  
  ```
{
  "token": "your_jwt_token",
  "bookid": 1
}

### Book_Author Management

- **Register Book Author**  
  Endpoint: `/book_author/register`  
  Method: `POST`  
  Payload:  
  ```
  {
  "token": "your_jwt_token",
  "bookid": 1,
  "authorid": 1
  }

  - **Show Book Author**  
  Endpoint: `/book_author/show`  
  Method: `GET`  
  Payload:  
  ```
{
  "Authorization": "Bearer your_token"
}

  - **Update Book Author**  
  Endpoint: `/book_author/update`  
  Method: `PUT`  
  Payload:  
  ```
{
  "token": "your_jwt_token",
  "collectionid": 1,
  "bookid": 1,
  "authorid": 1
}

  - **Delete Book Author**  
  Endpoint: `/book_author/update`  
  Method: `DELETE`  
  Payload:  
  ```
{
  "token": "your_jwt_token",
  "collectionid": 1
}
