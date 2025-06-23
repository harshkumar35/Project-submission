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

### 📝 Submission Instructions

1. Upload your project to GitHub or GitLab.
2. Include a short `README.md` with:

   * Setup instructions
   * How routing works
   * Any bonus you implemented
3. Deadline: **1 week**
4. Bonus points for:

   * Logging clarity
   * Clean and modular Docker setup
   * Healthcheck or automated test script

