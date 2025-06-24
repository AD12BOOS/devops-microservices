# 🐳 DevOps Microservices with NGINX Reverse Proxy



This project demonstrates a containerized microservice architecture using **Go**, **NGINX**, and **Docker Compose**.  
It includes two lightweight REST APIs served via a reverse proxy and health-checked for availability.

---

## 📦 Architecture

```
                    +----------------+
                    |    Browser     |
                    +----------------+
                           |
                   http://localhost:8080
                           ↓
                 +---------------------+
                 |      NGINX Proxy     |
                 |     (Port 8080)      |
                 +---------------------+
                    |              |
         /service1  |              | /service2
                    ↓              ↓
           +--------------+   +--------------+
           |  Service 1   |   |  Service 2   |
           |  (Go App)    |   |  (Go App)    |
           +--------------+   +--------------+
```

---

## 🚀 Quick Start

```bash
git clone https://github.com/<your-username>/devops-microservices.git
cd devops-microservices
docker-compose up --build
```

Then open your browser:

- 🔗 http://localhost:8080/service1 → `{"message": "Hello from Service 1!"}`
- 🔗 http://localhost:8080/service2 → `{"message": "Hello from Service 2!"}`

---

## 🧪 Health Checks

Each Go service includes a Docker health check:

- `service1` health endpoint → `http://localhost:8081`
- `service2` health endpoint → `http://localhost:8082`

---

## 🔧 Technologies Used

- [x] Go (Golang)
- [x] Docker & Docker Compose
- [x] NGINX Reverse Proxy
- [x] GitHub Actions CI (optional)
- [x] Health Checks & Logs

---

## 📁 Folder Structure

```
.
├── docker-compose.yml
├── nginx/
│   ├── nginx.conf
│   └── Dockerfile
├── service_1/
│   ├── Dockerfile
│   ├── go.mod
│   └── main.go
├── service_2/
│   ├── Dockerfile
│   ├── go.mod
│   └── main.go
└── README.md
```

---

## ✍️ Author

**Adarsh Desai**  
📫 [GitHub Profile](https://github.com/<your-username>)

---

## ✅ License

This project is licensed under the MIT License.
