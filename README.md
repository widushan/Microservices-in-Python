## Microservices in Python (Flask + Docker + Kubernetes)

A tiny **Flask microservice** that shows host details, containerizes with **Docker**, and deploys to **Kubernetes** using **Helm**.

---

## What this project covers

- **Flask microservice**: Simple REST endpoints (`/`, `/health`, `/details`)
- **Templates**: Jinja2 HTML template for dynamic host/IP info
- **Dependencies**: Managing Python packages with `pip` and `requirements.txt`
- **Containerization**: Building images with `Dockerfile`
- **Local orchestration**: Running the app with `docker-compose`
- **Kubernetes**: Deployment and Service manifests
- **Helm chart**: Templated Kubernetes deployment under `webapp/`

---

## Quick start (local)

- **Create & activate a virtual environment**
  - `python -m venv venv`
  - Windows: `venv\Scripts\activate`
  - Linux/macOS: `source venv/bin/activate`
- **Install dependencies**
  - `pip install -r requirements.txt`
- **Run the Flask app**
  - `python src/app.py`
- Open `http://localhost:5000` in your browser.

---

## Run with Docker

- **Build the image**
  - `docker build -t microservices-in-python .`
- **Run the container**
  - `docker run -p 5000:5000 microservices-in-python`

---

## Deploy to Kubernetes

- **Apply raw manifests**
  - `kubectl apply -f kubernetes/deployment.yml`
  - `kubectl apply -f kubernetes/service.yml`
- **Or use the Helm chart**
  - `helm install webapp ./webapp`

---

## GitHub repository

You can find the source code and updates here:  
`https://github.com/widushan/Microservices-in-Python`



