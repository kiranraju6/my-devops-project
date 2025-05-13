# Docker Projects: Node.js, HTML, and Python

This repository demonstrates Docker setups for three types of projects:

- 🟢 Node.js Web App  
- 🌐 Static HTML Website  
- 🐍 Python Application  

---

## 🟢 Node.js Project

### 📦 Prerequisites
- Dockerfile
- index.js
- package.json

### Build the Docker Image
```
docker build -t node-js:latest .
```
Run the Docker Container
```
docker run -itd -p 3000:3000 node-js:latest
```
Run the Docker Container with name
```

```

Access the Application
Open your browser and visit:
```
http://65.2.6.82:3000/
```
### You will see a response like:
"Hello, Dockerized Node.js!"

---

## 🌐 HTML Project
### 📦 Prerequisites
- Dockerfile
- index.html
### Build the Docker Image
```
docker build -t html:latest .
```
Run the Docker Container
```
docker run -itd -p 8080:80 html:latest
```
Access the Static Site
Open your browser and visit:
```
http://65.2.6.82:8080/
```
### You will see your static HTML page:
"Hello, World!"

---

## 🐍 Python Project
### 📦 Prerequisites
- Dockerfile
- app.py
### Build the Docker Image
```
docker build -t python:latest .
```
Run the Docker Container
```
docker run -itd python:latest
```
Check Running Containers
```
docker ps -a
```
View Logs
```
docker logs <container_id>
```
Example:
```
docker logs a7a9c5e00305
```

---

## 🛠 Common Docker Commands
#### CommandS
#### Build Image		    
     **docker build -t name:tag .**
#### Run Container		  
     **docker run -itd -p host:container name:tag**
#### List Containers		
     **docker ps -a**
#### Stop Container		
     **docker stop <container_id>**
#### Remove Container	
     **docker rm <container_id>**
#### Remove Image		  
     **docker rmi name:tag**
#### View Logs		      
     **docker logs <container_id>**

---

**📌 Notes**
Replace **65.2.6.82** with your actual server IP if needed.

Ensure required ports (3000, 8080, etc.) are open in your firewall or cloud security group.

Make sure your Dockerfile is correctly configured in each project directory.
