# MLOPS-Docker-Masterclass

A hands-on project demonstrating Docker containerization with a simple Flask web application.

## 📋 Overview

This repository provides a practical example of containerizing a Python Flask application using Docker. It's designed as a learning resource for understanding Docker fundamentals in an MLOps context.

## 🚀 Features

- Simple Flask web application with a greeting form
- Dockerized deployment setup
- Lightweight Python 3.10 slim base image

## 📁 Project Structure

```
.
├── app.py              # Flask application
├── dockerfile          # Docker configuration
├── requirements.txt    # Python dependencies
├── projectflow.txt     # Project workflow documentation
├── bonus.txt           # Additional notes
├── LICENSE             # License information
└── README.md           # This file
```

## 🛠️ Prerequisites

- [Docker](https://docs.docker.com/get-docker/) installed on your machine
- Git (optional, for cloning the repository)

## ⚡ Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/MLOPS-Docker-Masterclass.git
cd MLOPS-Docker-Masterclass
```

### 2. Build the Docker Image

```bash
docker build -t mlops-docker-demo .
```

### 3. Run the Container

```bash
docker run -p 5001:5001 mlops-docker-demo
```

### 4. Access the Application

Open your browser and navigate to:
```
http://localhost:5001
```

Enter your name in the form and submit to see the greeting message!

## 🐳 Docker Commands Reference

| Command | Description |
|---------|-------------|
| `docker build -t mlops-docker-demo .` | Build the Docker image |
| `docker run -p 5001:5001 mlops-docker-demo` | Run the container |
| `docker run -d -p 5001:5001 mlops-docker-demo` | Run in detached mode |
| `docker ps` | List running containers |
| `docker stop <container_id>` | Stop a running container |
| `docker images` | List all images |
| `docker rmi mlops-docker-demo` | Remove the image |

## 📦 Dependencies

- Flask 2.3.2
- Werkzeug 2.3.6

## 🔧 Local Development (Without Docker)

```bash
# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the application
python app.py
```

## 📝 How It Works

1. The Flask app serves a simple HTML form at the root endpoint (`/`)
2. When you submit your name, it sends a POST request to `/greet`
3. The app responds with a personalized greeting message

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues and pull requests.

## 📄 License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.
