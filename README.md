
# Using Docker Images from Docker Hub: A Step-by-Step Guide
In this guide, I'll walk you through the process of pulling and running Docker images for both the backend and frontend of our application.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Pulling Docker Images](#pulling-docker-images)
3. [Running the Backend](#running-the-backend)
4. [Running the Frontend](#running-the-frontend)

## 1. Prerequisites

Before you begin, ensure that you have Docker installed on your system. You can download Docker Desktop for Windows or Mac, or install Docker Engine on Linux. Make sure Docker is up and running.

## 2. Pulling Docker Images

First, you'll need to pull the Docker images for both the backend and frontend from Docker Hub. Open your terminal or command prompt and use the following commands:

```bash
docker pull <backend-image-name>
docker pull <frontend-image-name>
```

Replace `<backend-image-name>` and `<frontend-image-name>` with the names of the Docker images you uploaded to Docker Hub.

#### My backend image - 
```bash 
aniket2409/21bcp229-aniket-backend
```
#### My frontend image - 
```bash
aniket2409/21bcp229-aniket-frontend
```


## 3. Running the Backend

Once you have pulled the backend Docker image, you can run it as a Docker container. Use the following command:

```bash
docker run -d --name=21bcp229-aniket-backend -e MONGO_URI=<mongo_uri> -p 5002:5001 <backend-image-name>
```

Replace `<backend-image-name>` with the name of the backend Docker image you pulled earlier. This command will run the backend container in detached mode and map port 5002 on your local machine to port 5001 in the container.

## 4. Running the Frontend

Similarly, you can run the frontend Docker container using the following command:

```bash
docker run -d --name=21bcp229-aniket-frontend -p 8080:8080 <frontend-image-name>
```

## 5. Using Docker compose

To run the backend and frontend containers together using Docker Compose, create a `docker-compose.yml` file with the following content:

```bash
docker compose up
```

## 6. Docker Desktop 

#### a. Images in docker desktop
![dockerdesktop](image.png)

#### b. Running containers in docker desktop

![containers](image-1.png)


That's it! You now have both the backend and frontend of the application running as Docker containers on your local machine. You can access the application by navigating to `http://localhost:8080` in your web browser.


#### Feel free to adjust the placeholders and commands as needed for your specific backend and frontend Docker images! Happy containerizing!