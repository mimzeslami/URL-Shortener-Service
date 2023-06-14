# URL Shortener Service

This is a URL shortener service implemented in Go. It allows users to shorten long URLs and retrieve the original long URL using the generated short URL.

## Getting Started

### Prerequisites

- Go 1.16 or higher
- Docker

### Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>

    cd <repository-name>
    ```

2. Build the Docker image:

   ```bash
   make up_build 
   ```

   The service should now be running on http://localhost:8081.


## Usage

### Shorten a URL

To shorten a long URL, make a GET request to /short endpoint with the longUrl parameter.

```bash
curl -X GET 'http://localhost:8081/short?longUrl=<long-url>'

```

### Retrieve the original URL

To retrieve the original URL, make a GET request to /long endpoint with the shortUrl parameter.

```bash
curl -X GET 'http://localhost:8081/long?shortUrl=<short-url>'

```

## Testing

To run the tests, run the following command:

```bash
make test
```








