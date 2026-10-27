# FetchFlow

A beginner-friendly JavaScript project demonstrating how to interact with REST APIs using the **Fetch API**, `async/await`, and `try...catch` for asynchronous operations and error handling.

## Overview

This project demonstrates how to retrieve data from an API using a GET request and submit user-provided data using a POST request. It uses HTML forms and JavaScript DOM manipulation to display API responses dynamically without requiring a page reload.

## Features

- **GET Request:** Fetches an existing post from a REST API.
- **POST Request:** Submits user-entered name and email data to an API.
- **Async/Await:** Handles asynchronous HTTP requests using modern JavaScript syntax.
- **Error Handling:** Uses `try...catch` to handle network errors and other exceptions.
- **HTTP Status Validation:** Checks `response.ok` to detect unsuccessful HTTP responses.
- **JSON Processing:** Uses `JSON.stringify()` to format API responses for display.
- **Form Handling:** Uses `event.preventDefault()` to prevent the browser's default form submission behavior.
- **DOM Manipulation:** Displays API responses and error messages directly on the webpage.

## Technologies Used

- HTML5
- JavaScript (ES6+)
- Fetch API
- JSON
- REST APIs

## API Used

This project uses [JSONPlaceholder](https://jsonplaceholder.typicode.com/), a free fake REST API for testing and prototyping.

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/posts/1` | Retrieves an existing post |
| POST | `/posts` | Simulates creating a new post |

## How It Works

### 1. GET Request

When the user clicks the **Get User** button:

1. JavaScript sends a GET request using `fetch()`.
2. `await` waits for the HTTP response.
3. `response.ok` checks whether the HTTP status indicates success.
4. `response.json()` parses the response body into a JavaScript object.
5. `JSON.stringify()` converts the object into formatted text.
6. The result is displayed in the `getOutput` paragraph.

### 2. POST Request

When the user submits the form:

1. The submit event is intercepted using `event.preventDefault()`.
2. The name and email values are collected into a JavaScript object.
3. `JSON.stringify()` converts the object into a JSON string.
4. A POST request sends the data with the `Content-Type: application/json` header.
5. The response is checked, parsed, and displayed in the `postOutput` paragraph.

### 3. Error Handling

Both operations use `try...catch` to handle errors.

- Network failures, such as a failed connection.
- HTTP errors detected by checking `response.ok` and throwing an error.
- JSON parsing errors.
- Other exceptions occurring within the `try` block.

Errors are logged to the browser console, and a message is displayed on the webpage.

## Project Structure

```text
fetch-api-project/
├── index.html
└── README.md
```

The `index.html` file contains the HTML structure, form elements, and JavaScript logic.

## Getting Started

### Prerequisites

- A modern web browser.
- An internet connection to access JSONPlaceholder.

### Installation and Execution

1. Clone the repository:

   ```bash
   git clone <your-repository-url>
   ```

2. Navigate to the project directory:

   ```bash
   cd fetch-api-project
   ```

3. Open `index.html` in your browser, or use the Live Server extension in Visual Studio Code.

4. Click **Get User** to retrieve an existing post.

5. Enter a name and valid email address, then click **Submit** to test the POST request.

## Key Concepts Learned

- Making HTTP requests with the Fetch API.
- Understanding GET and POST methods.
- Working with Promises and `async/await`.
- Parsing JSON responses with `response.json()`.
- Converting JavaScript objects to JSON using `JSON.stringify()`.
- Validating HTTP responses with `response.ok`.
- Handling errors using `try...catch`.
- Handling form submission events.
- Manipulating webpage content using the DOM.

## Limitations

JSONPlaceholder is a mock API. POST requests return a simulated response but do not permanently save submitted data. This project does not include a custom backend, database, authentication, or persistent storage.

## Future Improvements

- Add a loading indicator while requests are in progress.
- Disable the submit button during submission.
- Display user-friendly error messages.
- Fetch and display multiple posts.
- Add input validation and form reset functionality.
- Integrate a custom backend and database for persistent data storage.

## License

This project is intended for learning and educational purposes. You may modify and extend it for your own projects.
