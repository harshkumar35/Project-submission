### 🧪 **DevOps Intern Assignment: Nginx Reverse Proxy + Docker**

You are expected to set up a simple system where:

1. **Two Dockerized backend services** (can be dummy services) run on different ports.
2. An **Nginx reverse proxy** (also in a Docker container) routes:

   * `/service1` requests to backend service 1
   * `/service2` requests to backend service 2
3. All services must be accessible via a single port (e.g., `localhost:8080`).

---

### ✅ **Requirements**

1. Use Docker Compose to bring up the entire system.
2. Each backend service should respond with a JSON payload like:

   ```json
   {"service": "service1"}
   ```
3. The Nginx config should support:

   * Routing based on URL path prefix (`/service1`, `/service2`)
   * Logging incoming requests with timestamp and path
4. The system should work with a single command:

   ```bash
   docker-compose up --build
   ```
5. Bonus: Add a health check for both services and show logs of successful routing.

---

### 📁 Suggested Project Structure

```
.
├── docker-compose.yml
├── nginx
│   ├── default.conf
│   └── Dockerfile
├── service_1
│   ├── app.py
│   └── Dockerfile
├── service_2
│   ├── app.py
│   └── Dockerfile
└── README.md
```

---

### 📦 Tech Constraints

* Nginx must run in a Docker container, not on host
* Use bridge networking (no host networking)

---

# 🚀 DevOps Assignment – NGINX Reverse Proxy with Docker Compose

This project demonstrates a containerized microservice setup using Docker Compose. It includes two backend services written in Go and Python Flask, both routed through an NGINX reverse proxy on port `8080`.

---

## 📁 Project Structure

```

.
├── docker-compose.yml
├── nginx/
│   ├── Dockerfile
│   └── nginx.conf
├── service\_1/
│   ├── Dockerfile
│   ├── main.go
├── service\_2/
│   ├── Dockerfile
│   ├── app.py
│   └── pyproject.toml
└── README.md

````

---

## 🔧 Setup Instructions

### Prerequisites:
- Docker
- Docker Compose

### Run the project:

```bash
docker compose up --build
````

---

## 🌐 NGINX Reverse Proxy (localhost:8080)

| Endpoint          | Description   | Backend Service     |
| ----------------- | ------------- | ------------------- |
| `/service1/ping`  | Health check  | Go (port 8001)      |
| `/service1/hello` | Hello message | Go (port 8001)      |
| `/service2/ping`  | Health check  | Python Flask (8002) |
| `/service2/hello` | Hello message | Python Flask (8002) |

---

## 🧪 Testing the Services

```bash
curl http://localhost:8080/service1/ping
curl http://localhost:8080/service1/hello
curl http://localhost:8080/service2/ping
curl http://localhost:8080/service2/hello
```

Or open them in your browser.

---

## 📦 Features

* ✅ NGINX reverse proxy container
* ✅ Dockerized Go & Python services
* ✅ Path-based routing via NGINX
* ✅ Healthchecks for both services
* ✅ Logging of all incoming requests in NGINX
* ✅ Single network using Docker bridge

---

## 💡 Bonus (Implemented)

* Logging with timestamp and request path in `nginx.conf`
* Healthcheck routes to auto-verify service readiness
* Clean Docker structure (Dockerfile for each service)

---

## 📤 Submission

* ✅ Code pushed to GitHub: [https://github.com/harshkumar35/Project-submission](https://github.com/harshkumar35/Project-submission)

---

## 👨‍💻 Author

**Harsh Kumar**
B.Tech CSBS, GGITS
📧 [harshku612810@gmail.com](mailto:harshku612810@gmail.com)
🌐 [LinkedIn](https://www.linkedin.com/in/harshk251103/)

---

🎯 Thank you! This concludes the assignment.


