# Consuming REST from JavaScript

This repository demonstrates how to consume REST APIs from JavaScript using `fetch()` and modern asynchronous patterns like `async` and `await`.

## Features
- Making REST API requests with the `fetch()` API
- Handling different HTTP methods (GET, POST, PUT, DELETE)
- Parsing JSON responses and error handling
- Asynchronous JavaScript with `async`/`await` and promises

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/UCN-LANY-Technology3/ConsumingRESTFromJavaScript.git
   ```
2. Open the project in your preferred code editor (e.g., VS Code).
3. Serve the files using a local server (e.g., using `Live Server` in VS Code or setting up a basic HTTP server in Node.js).
4. Open `index.html` in a web browser to run the JavaScript code.

## Usage
The project provides examples of sending various REST API requests (GET, POST, PUT, DELETE) to a sample API.

### Example Usage:

#### Fetching Data:
```javascript
async function fetchData() {
   try {
      const response = await fetch('https://api.example.com/data');
      const data = await response.json();
      console.log(data);
   } catch (error) {
      console.error('Error:', error);
   }
}

fetchData();
```

#### Sending Data with POST:
```javascript
async function sendData(data) {
   const response = await fetch('https://api.example.com/data', {
      method: 'POST',
      headers: {
         'Content-Type': 'application/json'
      },
      body: JSON.stringify(data)
   });
   const result = await response.json();
   console.log(result);
}
```

## Contributing
Contributions are welcome! Feel free to fork this repository, make your changes, and submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
