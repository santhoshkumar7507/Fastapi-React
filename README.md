<h1 align="center">
  <br>
  Todo App: FastAPI + React + MongoDB
  <br>
</h1>

<h4 align="center">A premium, full-stack Task Management application featuring a stunning Glassmorphism UI.</h4>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#quick-start">Quick Start</a>
</p>

---

## 🌟 Features

- **Stunning UI/UX**: Completely redesigned with a modern, dark-mode glassmorphism aesthetic. Features dynamic hover effects, smooth transitions, and sleek gradient typography.
- **Lightning Fast Backend**: Powered by FastAPI, offering incredibly fast routing and asynchronous operations out of the box.
- **Seamless Data Persistence**: Integrated with MongoDB for reliable, document-based storage.
- **Fully Dockerized**: No complicated local setup. Run the entire frontend, backend, database, and reverse proxy with a single Docker command.

## 💻 Tech Stack

### Frontend
- **React 19**
- Vanilla CSS (Glassmorphism + Dark Mode theme)
- Axios for API communication
- React Icons

### Backend
- **Python 3.11**
- **FastAPI**
- Uvicorn (ASGI server)
- Motor (Asynchronous Python driver for MongoDB)

### Infrastructure
- **Docker & Docker Compose**
- **Nginx** (Reverse Proxy)
- **MongoDB** (Containerized or Cloud via Atlas)

---

## 🏗 Architecture

The application runs seamlessly via `docker-compose` utilizing four distinct containers:

1. **`frontend`**: Serves the React application on port `3000`. Hot-reloading enabled for development.
2. **`backend`**: Serves the FastAPI endpoints on port `3001` (mapped to `8001` on host).
3. **`mongodb`**: Local MongoDB instance ensuring persistent storage via Docker volumes.
4. **`nginx`**: A reverse proxy that intelligently routes traffic between the frontend and backend.

---

## 🚀 Quick Start

### Prerequisites
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and running.
- Git (optional).

### Installation & Execution

1. **Clone the repository** (or navigate to your local project folder):
   ```bash
   cd "Week 1 (FastApi React)"
   ```

2. **Configure Environment Variables**:
   Ensure you have a `.env` file at the root of the project containing your MongoDB Connection string. For local Docker usage, the file should look like this:
   ```env
   MONGODB_URI='mongodb://mongodb:27017/todo_app'
   ```

3. **Spin up the application**:
   Run the following command to build the images, install dependencies automatically, and start the services in the background:
   ```bash
   docker-compose up -d --build
   ```

4. **Access the App**:
   - **Frontend UI**: [http://localhost:3000](http://localhost:3000)
   - **FastAPI Swagger UI**: [http://localhost:8001/docs](http://localhost:8001/docs)

### Stopping the App

To shut down the application and cleanly stop all containers:
```bash
docker-compose down
```

---

<p align="center">
  <i>Designed and developed for high performance, ease-of-use, and stunning aesthetics.</i>
</p>
