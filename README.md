
# Simple Web Server in Go

This project is a basic web server written in Go that demonstrates handling static files, routing, and processing HTML form submissions. The server has the following features:

- Serves static files from the `./static` directory.
- Routes HTTP requests to custom handlers for `/hello` and `/form`.
- Processes POST form submissions and displays submitted data.

---

## Project Structure

```
.
├── main.go         # Main Go file that defines the web server
├── static
│   ├── index.html  # A simple static HTML file served as the homepage
│   ├── form.html   # A form to collect user input
```

---

## Features

1. **Static File Server**  
   Serves files located in the `./static` directory.

2. **Custom Handlers**  
   - `/hello`: Responds to GET requests with a greeting.
   - `/form`: Handles POST form submissions and displays submitted data.

3. **HTML Forms**  
   The form located at `static/form.html` collects a user's name and address.

---

## Getting Started

### Prerequisites

- Install [Go](https://golang.org/doc/install) (1.16 or later is recommended).

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/simple-web-server.git
   cd simple-web-server
   ```

2. Ensure the project structure is as follows:
   ```
   .
   ├── main.go
   ├── static
       ├── index.html
       ├── form.html
   ```

3. Build and run the server:
   ```bash
   go run main.go
   ```

4. Open a web browser and navigate to `http://localhost:8080`.

---

## Usage

### Available Routes

- `/`: Serves `index.html` from the `./static` directory.
- `/hello`: Responds with "Hello!" for GET requests.
- `/form`: Processes form submissions via POST requests.

### Submitting the Form

1. Navigate to `http://localhost:8080/form.html`.
2. Fill in your name and address.
3. Submit the form. The server will display the submitted values.

---

## Example Outputs

### `/hello`
Request:
```bash
curl http://localhost:8080/hello
```
Response:
```
Hello!
```

### `/form` (POST)
Request:
```bash
curl -X POST -d "name=John&address=123 Street" http://localhost:8080/form
```
Response:
```
POST request successful
Name = John
Address = 123 Street
```

---

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue for any improvements or bugs.

---

## License

This project is licensed under the MIT License. See `LICENSE` for details.
