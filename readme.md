# Kubernetes Nginx Static Website

A simple static website built with **HTML & CSS**, served using **Nginx**, containerized with **Docker**, and deployed on **Kubernetes**.

This project demonstrates the complete workflow of containerizing and deploying a static website using Kubernetes.

---

## 🚀 Features

* Responsive static website
* Dockerized using Nginx
* Kubernetes Deployment
* Kubernetes Service (LoadBalancer)
* Multiple Pod replicas
* Easy to customize and deploy

---

## 🛠️ Technologies Used

* HTML5
* CSS3
* Nginx
* Docker
* Kubernetes

---

## 📁 Project Structure

```text
.
├── index.html
├── style.css
├── Dockerfile
├── deployment.yaml
├── README.md
└── LICENSE
```

---

## 🌐 Website Preview

The website contains three main sections:

* Docker
* Nginx
* Kubernetes

along with a clean, responsive user interface.

---

# 🐳 Docker

## Build the Docker Image

```bash
docker build -t <your-dockerhub-username>/nginx_static_website .
```

## Run the Container Locally

```bash
docker run -d -p 8080:80 <your-dockerhub-username>/nginx_static_website
```

Open your browser:

```
http://localhost:8080
```

---

# ☁️ Push Image to Docker Hub

Login to Docker Hub:

```bash
docker login
```

Tag the image:

```bash
docker tag nginx_static_website <your-dockerhub-username>/nginx_static_website:latest
```

Push the image:

```bash
docker push <your-dockerhub-username>/nginx_static_website:latest
```

---

# ⚠️ Important Notice

The original Docker image referenced in this project was:

```text
vinitparmar03/nginx_static_website
```

This image has been removed from Docker Hub and is no longer publicly available.

Because of this, the Kubernetes deployment **will not run successfully** unless you build and push your own Docker image.

After pushing your image to Docker Hub, update the image name inside **deployment.yaml**.

Replace:

```yaml
image: vinitparmar03/nginx_static_website
```

with

```yaml
image: <your-dockerhub-username>/nginx_static_website:latest
```

---

# ☸️ Kubernetes Deployment

Deploy the application:

```bash
kubectl apply -f deployment.yaml
```

Verify the deployment:

```bash
kubectl get deployments
```

Check Pods:

```bash
kubectl get pods
```

Check Services:

```bash
kubectl get svc
```

Describe Deployment:

```bash
kubectl describe deployment nginx-deployment
```

---

# 📄 Kubernetes Resources

## Deployment

* Deployment Name: `nginx-deployment`
* Replicas: **2**
* Container Port: **80**

## Service

* Service Type: `LoadBalancer`
* Service Port: **80**
* Target Port: **80**

---

# 📚 What You'll Learn

This project demonstrates:

* Building a static website
* Creating a Docker image
* Running containers with Docker
* Writing a Dockerfile
* Creating Kubernetes Deployments
* Using Labels and Selectors
* Creating Kubernetes Services
* Exposing applications using LoadBalancer
* Managing multiple Pod replicas

---

# ▶️ Quick Start

Clone the repository:

```bash
git clone https://github.com/<your-github-username>/Kubernetes_nginx_static_web.git
```

Go to the project directory:

```bash
cd Kubernetes_nginx_static_web
```

Build the Docker image:

```bash
docker build -t <your-dockerhub-username>/nginx_static_website .
```

Push it to Docker Hub:

```bash
docker push <your-dockerhub-username>/nginx_static_website
```

Update the image name inside `deployment.yaml`.

Deploy to Kubernetes:

```bash
kubectl apply -f deployment.yaml
```

Verify:

```bash
kubectl get all
```

---

# 👨‍💻 Author

**Vinit Kumar Parmar**

GitHub: https://github.com/Vinitparmar03

---

## 📢 Connect With Me

If you found this project helpful, feel free to connect with me and check out my work.

* **GitHub:** https://github.com/Vinitparmar03
* **LinkedIn:** https://www.linkedin.com/in/vinit-kumar-parmar-22522a215/
* **LinkedIn Project Post:** https://www.linkedin.com/posts/vinit-kumar-parmar-22522a215_kubernetes-docker-nginx-ugcPost-7477770731657994241-DPD7/?utm_source=share&utm_medium=member_desktop&rcm=ACoAADZRDr0B3jGUgimvN4mtmvOEEJqmA9dQEvQ

If you like this project, don't forget to ⭐ star the repository!

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

1. Fork the repository.
2. Create a new branch.
3. Commit your changes.
4. Push your branch.
5. Open a Pull Request.

---

# 📄 License

This project is licensed under the **MIT License**.

See the **LICENSE** file for more information.
