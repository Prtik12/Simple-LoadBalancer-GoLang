# Load Balancer Golang

A simple load balancer built in Go using reverse proxy and round-robin routing.

---

<img width="1920" alt="Screenshot 2025-05-27 at 1 15 53 AM" src="https://github.com/user-attachments/assets/d5a1450b-ff44-4cc4-aecc-c30037e7e863" />


---

## Features

- Round-robin request distribution
- Reverse proxy using Go's `httputil`
- Pluggable server interface
- Minimal and easy-to-read structure

## How it Works

The load balancer receives HTTP requests and forwards them to a list of predefined backend servers in a round-robin manner using `httputil.NewSingleHostReverseProxy`.

```go
servers := []Server{
    newSimpleServer("https://www.facebook.com"),
    newSimpleServer("https://github.com"),
    newSimpleServer("https://x.com"),
}
````

## Getting Started

Clone the repository and run the load balancer:

```bash
git clone https://github.com/yourusername/go-load-balancer.git
cd go-load-balancer
go run main.go
```

By default, it listens on `localhost:8000`.

Test it using:

```bash
curl http://localhost:8000
```


