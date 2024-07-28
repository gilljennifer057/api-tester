# API Testing Script

This script is designed to interact with a REST API to perform CRUD (Create, Read, Update, Delete) operations on "todos". It uses Axios for HTTP requests and Node.js for scripting.

## Overview

The script supports the following operations:

- Fetch all todos
- Create a new todo
- Update an existing todo
- Delete a todo

## Dependencies

- `axios`: For making HTTP requests.
- `process`: For handling command-line arguments.

## Constants

- `BASE_URL`: The base URL of the API server. Default is `http://localhost:9000`.
- `endpoint`: The API endpoint for "todos". Default is `todos`.
- `createPayload`: The payload for creating a new todo. Default is `{ text: "created" }`.
- `updatePayload`: The payload for updating an existing todo. Default is `{ text: "updated" }`.

## Functions

### `fetchTodos()`

Fetches the list of todos from the API.

- **Method:** `GET`
- **Endpoint:** `/todos`

Logs the result of the request or an error message if the request fails.

### `createTodo()`

Creates a new todo in the API.

- **Method:** `POST`
- **Endpoint:** `/todos`
- **Payload:** `{ text: "created" }`

Logs the result of the request or an error message if the request fails.

### `updateTodo(id)`

Updates an existing todo in the API.

- **Method:** `PUT`
- **Endpoint:** `/todos/:id`
- **Payload:** `{ text: "updated" }`
- **Parameters:**
  - `id`: The ID of the todo to update.

Logs the result of the request or an error message if the request fails.

### `deleteTodo(id)`

Deletes a todo from the API.

- **Method:** `DELETE`
- **Endpoint:** `/todos/:id`
- **Parameters:**
  - `id`: The ID of the todo to delete.

Logs the result of the request or an error message if the request fails.

### `testAPI()`

Handles command-line arguments and calls the appropriate function based on the provided command.

- **Arguments:**
  - `r`: Fetches todos.
  - `c`: Creates a new todo.
  - `u <id>`: Updates a todo with the specified ID.
  - `d <id>`: Deletes a todo with the specified ID.

## Usage

To use this script, run it from the command line with the desired operation and parameters:

```bash
node script.js <command> [id]
