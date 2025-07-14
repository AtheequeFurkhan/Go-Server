# Go Web Server

A simple HTTP web server built with Go that serves static files and handles form submissions.

## Features

- **Static File Serving**: Serves HTML files and other static content from the `static` directory
- **Form Handling**: Processes form submissions with name and email fields
- **RESTful Endpoints**: Multiple API endpoints for different functionalities
- **Error Handling**: Proper HTTP status codes and error responses

## Project Structure

```
Go-Server/
├── README.md
└── static/
    ├── main.go          # Main server application
    ├── index.html       # Home page
    └── form.html        # Contact form page
```

## Endpoints

### Static Routes

- `GET /` - Serves the main index.html page
- `GET /form.html` - Serves the contact form page

### API Routes

- `GET /hello` - Returns a simple "Hello!" message
- `POST /form` - Processes form data and returns submitted values
- `GET /submit` - Returns a submission confirmation message

## Getting Started

### Prerequisites

- Go 1.16 or higher installed on your system

### Installation

1. Clone or download this repository:

```bash
git clone <repository-url>
cd Go-Server
```

2. Navigate to the static directory:

```bash
cd static
```

3. Run the server:

```bash
go run main.go
```

4. Open your web browser and visit:

```
http://localhost:8080
```

## Usage

### Viewing the Home Page

Navigate to `http://localhost:8080` to see the static web page.

### Using the Contact Form

1. Go to `http://localhost:8080/form.html`
2. Fill out the name and email fields
3. Click Submit to see the form data processed

### Testing API Endpoints

- **Hello endpoint**: Visit `http://localhost:8080/hello`
- **Submit endpoint**: Visit `http://localhost:8080/submit`

## Code Overview

The server is built using Go's standard `net/http` package and includes:

- **Static file server**: Serves files from the `static` directory
- **Form handler**: Processes POST requests with form data
- **Hello handler**: Simple GET endpoint
- **Submit handler**: GET endpoint for form submissions

## Development

To modify the server:

1. Edit `static/main.go` for server logic changes
2. Modify HTML files in the `static` directory for frontend changes
3. Restart the server to see changes

## Port Configuration

The server runs on port 8080 by default. To change the port, modify the following line in `main.go`:

```go
http.ListenAndServe(":8080", nil)
```

## Error Handling

The server includes proper error handling for:

- 404 errors for invalid routes
- 405 errors for unsupported HTTP methods
- Form parsing errors

## License

This project is open source and available under the [MIT License](LICENSE).
