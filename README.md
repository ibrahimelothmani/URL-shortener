# URL Shortener

A simple URL shortener service written in Go.

## Features

- Shorten long URLs to short hashes
- Redirect short URLs to their original long URLs
- Delete shortened URLs
- In-memory storage (no database required)
- RESTful API endpoints

## Endpoints

- `POST /add`  
  Shorten a URL.  
  **Request Body:**  
  ```json
  { "url": "https://example.com" }
  ```
  **Response:**  
  ```json
  {
    "shortened_url": "http://localhost:8080/r/xxxxxxxxxx",
    "long_url": "https://example.com"
  }
  ```

## Requirements
Go 1.21 or later

## Notes
All data is stored in memory and will be lost when the server restarts.
Uses gorilla/mux for routing.